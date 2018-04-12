####VeeValidate [官方文档地址](http://vee-validate.logaretm.com/)

#####安装
>不同版本会有一些改动，比如错误信息会存放在errors字段中，而版本更新之后发现，错误信息存放在了其他字段中， 此配置有些版本会报错。（当前使用版本2.0.0-rc.25）

```
npm install vee-validate --save
```
<br>

#####常规使用
``` 
import zh_CN from 'vee-validate/dist/locale/zh_CN';
import VeeValidate, { Validator } from 'vee-validate';

Vue.use(VeeValidate);
// 提示信息汉化
Validator.addLocale(zh_CN); 
Vue.use(VeeValidate, {
	errorBagName: 'errors', 
	fieldsBagName: 'fields',
	delay: 100,   
	locale: 'zh_CN', 
	strict: true,  
	enableAutoClasses: true,
	events: '', 
	inject: true
}); 

```
<br>


#####自定义错误信息提示
>需要在常规使用配置下追加如下配置

```
import VueI18n from 'vue-i18n';  // 需安装vue-i18n包
Vue.use(VueI18n); 

// 配置中英文消息提示， message的key值为对应验证输入框的name属性
const messages = {
	en: {
		message: {
			hello: 'word hello',
		}
	},
	zh: {
		message: {
			hello: '你好',
			mobile: '手机号',
			psw: '密码',
			psw2: '密码',
			account_number: '卡号',
			username: '姓名', 
		}
	}
}

const i18n = new VueI18n({
	locale: 'zh', // set locale
	messages, // set locale messages
})


new Vue({
	router, 	 ,
	i18n    // 实例化vue时需追加此配置
}).$mount('#app');

```


#####扩展验证规则
```
import { Validator } from 'vee-validate';

Validator.extend('mobile', {
    messages: {
        zh_CN:(field, args) => '必须是11位手机号码',
        en:(field, args) => '必须是11位手机号码',
    },
 
    validate: (value, args) => {
       return value.length == 11 && /^((13|14|15|17|18)[0-9]{1}\d{8})$/.test(value)
    }
});

Validator.extend('int', {
    messages: {
        zh_CN:(field, args) => '必须是整数',
        en:(field, args) => '必须是整数',
    },
 
    validate: (value, args) => {
       return /^[1-9]{1,}\d*$/.test(value)
    }
})

```

#####在组件中使用

```
<div class="column is-12">
	<label class="label">Email (1s delay)</label>
	<p class="control has-icon has-icon-right">
		<input name="email" v-validate="'required|email'" data-vv-delay="1000" :class="{'input': true, 'is-danger': errors.has('email') }" type="text" placeholder="Email">
		<i v-show="errors.has('email')" class="fa fa-warning"></i>
	</p>
</div>
```
