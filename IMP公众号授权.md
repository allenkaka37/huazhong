BasePath : http://IP:8080/imp/

1.获取组件appId和预授权码

接口名：author/tpPlatformAuthor!getWxMpPreAuthorInfo.action

请求参数：无

返回结果:
``` javascript
{
    "data": {
        "redirect_uri": "http://johnccheng.huazhongtimes.com/imp/author/tpPlatformAuthor!wxMpPreAuthorCallBack.action", //无作用 忽视
        "preAuthCode": "preauthcode@@@yee7bs_GFobGRH7A5kTeI7y8h4mJCnmhjW4dSMYH_O3CwclgpUo2WHZlOP7hOEP1", //托管平台预授权码
        "expiresTime": 1460701351524, //失效时间
        "componentAppid": "wxa0833b06b5cd5f8e", //组建ID
        "userId":1234 //当前发起授权的用户ID
    },
    "success": true
}
```

2.跳转至微信平台进行托管
跳转地址：
https://mp.weixin.qq.com/cgi-bin/componentloginpage
参数：
component_appid ：组建ID
pre_auth_code ：预授权码
redirect_uri  ： http://johnccheng.huazhongtimes.com/imp/author/tpPlatformAuthor!wxMpPreAuthorCallBack.action?userid=${userId} (通过之前接口获取)

返回结果：无
