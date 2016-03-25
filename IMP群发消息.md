

BasePath : http://IP:8080/imp/

** 1. 获取群发消息列表 **

`接口名：massmessageController!getMassmessageList.action?currentPage=1&pageSize=20&mpUserName=gh_853df56d4234`

`参数： currentPage 当前页码 pageSize 每页数量 mpUserName 公众号原始ID`

`返回数据：`
```javascript
{
	"buttons": [{
		"type": null,
		"name": "我的拿吧",
		"key": null,
		"url": null,
		"subButtons": [{
			"type": "view",
			"name": "流量中心",
			"key": null,
			"url": "http://naba.51094.com/naba/usercenter/userCenter.action?authType=0",
			"subButtons": []
		},
		{
			"type": "view",
			"name": "客服",
			"key": null,
			"url": "http://naba.51094.com/naba/customerServices/customerServices.action?authType=0",
			"subButtons": []
		},
		{
			"type": "view",
			"name": "推拿手",
			"key": null,
			"url": "http://naba.51094.com/naba/pushHand/pushHand.action?authType=0",
			"subButtons": []
		},
		{
			"type": "view",
			"name": "正式个人中心",
			"key": null,
			"url": "http://www.5amg.cn/naba/usercenter/userCenter.action?authType=0",
			"subButtons": []
		}]
	},
	{
		"type": "view",
		"name": "天天赚流量",
		"key": null,
		"url": "http://naba.51094.com/naba/activity/activity.action?activityId=6&activityType=1&authType=1",
		"subButtons": []
	},
	{
		"type": null,
		"name": "活动赚流量",
		"key": null,
		"url": null,
		"subButtons": [{
			"type": "view",
			"name": "下载赚流量",
			"key": null,
			"url": "http://naba.51094.com/naba/websiteDownload/websiteDownLoad.action?authType=0",
			"subButtons": []
		},
		{
			"type": "view",
			"name": "关注送流量模版",
			"key": null,
			"url": "http://naba.51094.com/naba/activity/activity.action?activityId=7&activityType=5&authType=1",
			"subButtons": []
		}]
	}],
	"matchRule": null
}
```
** 2. 群发消息 **

`接口名：massmessageController!sendMessage.action?mpUserName=gh_853df56d4234&type=1&sendMode=3&content=就开始地方看见看&mediaId=rORSJmzgtNIXcm7eXyWlyY5Qdsogb89DJRUTFJ_sc9Xuvem6UD21ySZtGK97_4Sl&groupIds=0,1&openIds=ssdjfksdkfj,sddkjfksdj`

`参数: mpUserName 公众号原始ID|type 消息类型 1:文本;2:图文;3:多图文|sendMode 群发方式 1:分组群发;2:指定粉丝;3:全部粉丝|mediaId 素材ID|groupIds 微信组ID, 多个中间用英文逗号隔开|openIds 粉丝openId（要求大于2，小于10000，中间英文逗号隔开）`

`返回数据:`

```javascript
{
	"message": "同步成功",
	"success": true
}
```
