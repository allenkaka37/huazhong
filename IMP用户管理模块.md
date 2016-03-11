

BasePath : http://IP:8080/imp/

**1.获取用户注册短信验证码**

`接口名：userController!getSMSVerifyCode.action?phoneNum=15986793724&verifyCode=abcd`

`参数：phoneNum 电话号码 verifyCode 图片验证码`

`返回数据：`
```javascript
{
	"data": {
		"SMSVerifyCode": "981179"  短信验证码
	},
	"success": true 成功返回数据
}

{
	"message": "注册手机号码格式不正确", 错误信息
	"success": false 失败返回数据
}
```
**2.获取图片验证码**

`接口名：userController!getVerifyCode.action?phoneNum=15986793724`

`参数: phoneNum 电话号码`

`返回数据:`

`验证码图片流`


**3. 验证将要注册的用户名及手机号码是否被注册过**

`接口名：userController!verifyRegisterInfo.action?userName=Karl&phoneNum=15986793724`

`参数：userName 用户名 phoneNum 电话号码`

`返回数据：`
```javascript
{
	"message": ""
	"success": true 成功返回数据
}

{
	"message": "该用户名已被注册过，请更换其他用户名
	"success": false
}
```

**4.用户注册**

`接口名：userController!userRegister.action?userName=karl&phoneNum=15986793724&password=123456&smsVerifycode=9527`

`参数：userName 用户名 password 密码 phoneNum 电话号码 smsVerifycode 短信验证码`

`返回数据:`
```javascript
{
	"message": "",
	"success": true
}

{
	"message": "验证码已过期",
	"success": false
}
```

**5.用户登录**

`接口名：userController!login.action?userName=karl&password=123456&verifyCode=abcd&isRememberPwd=1`

`参数：userName 用户名 password 密码 verifyCode 验证码 isRememberPwd 是否记住密码(1为记住，0为不记住)`

`返回数据:`
```javascript
{
	"message": "",
	"success": true
}

{
	"message": "用户名错误或已被禁用",
	"success": false
}
```

**6.用户登出**

`接口名：userController!logout.action`
`参数：无`

`返回数据: 无`


**7.修改密码**

`接口名：userController!editPassword.action?oldPassword=123456&newPassword=111111&smsVerifycode=778111`

`参数：oldPassword 旧密码 newPassword 新密码 smsVerifycode 短信验证码 `

`返回数据:`
```javascript
{
	"message": "",
	"success": true
}

{
	"message": "旧密码错误",
	"success": false
}
```

**8.忘记密码，重置密码**

`接口名：userController!resetPassword.action?userName=karl&phoneNum=15986793724&smsVerifycode=778111&password=111111`

`参数：userName 用户名 phoneNum 电话号码 smsVerifycode 短信验证码 password 重置的密码`

`返回数据:`
```javascript
{
	"message": "",
	"success": true
}

{
	"message": "用户名和电话号码不匹配",
	"success": false
}
```

**9.忘记密码重置时，验证用户名、电话是否有效**

`接口名：userController!verifyNamePhoneValid.action?userName=karl&phoneNum=15986793724`

`参数：userName 用户名 phoneNum 电话号码`

`返回数据:`
```javascript
{
	"message": "",
	"success": true
}

{
	"message": "用户名和电话号码不匹配",
	"success": false
}
```
