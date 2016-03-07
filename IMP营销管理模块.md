BasePath : http://IP:8080/imp/

**1.添加营销活动**
```javascript
接口名称:  activityController!saveActivityInfo.action
参数描述:  type			对应活动类型:1-关注,2-注册,3-下载
	   name			名字:type=1 公众号名,type =2和3 应用名
	   maxmember		参与人数上限
	   guideUrl		推广地址:type=1 公众号的关注地址,type=2 注册页面地址
	   appType		应用类型:理财,游戏,社交,开发等.英文逗号分隔
	   registerType		注册方式:1-手机号,2-邮箱
	   sendFlag		是否发送用户记录至第三方.1-发送,0-不发
	   sendUrl		第三方的接收消息地址
	   shortDescription	下载类的简要描述,可做关注类的标题
	   appStoreId		苹果应用商店id
	   tencentStore		腾讯应用宝地址
	   androidUrl		安卓下载地址
	   iosSize		ios版本大小
	   androidSize		android版本大小
```
