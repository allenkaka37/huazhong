

BasePath : http://IP:8080/imp/

** 1. 获取微信菜单信息 **

`接口名：mpwxmenuController!getMpwxmenu.action?mpUserName=gh_853df56d4234`

`参数： mpUserName 公众号原始ID`

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
** 2.生效到微信 **

`接口名：mpwxmenuController!effectMpwxmemu.action?mpUserName=gh_853df56d4234&menus=[{"type":null,"name":"我的拿吧","key":null,"url":null,"subButtons":[{"type":"view","name":"流量中心","key":null,"url":"http://naba.51094.com/naba/usercenter/userCenter.action?authType=0","subButtons":[]},{"type":"view","name":"客服","key":null,"url":"http://naba.51094.com/naba/customerServices/customerServices.action?authType=0","subButtons":[]},{"type":"view","name":"推拿手","key":null,"url":"http://naba.51094.com/naba/pushHand/pushHand.action?authType=0","subButtons":[]},{"type":"view","name":"正式个人中心","key":null,"url":"http://www.5amg.cn/naba/usercenter/userCenter.action?authType=0","subButtons":[]}]},{"type":"view","name":"天天赚流量","key":null,"url":"http://naba.51094.com/naba/activity/activity.action?activityId=6&activityType=1&authType=1","subButtons":[]},{"type":null,"name":"活动赚流量","key":null,"url":null,"subButtons":[{"type":"view","name":"下载赚流量","key":null,"url":"http://naba.51094.com/naba/websiteDownload/websiteDownLoad.action?authType=0","subButtons":[]},{"type":"view","name":"关注送流量模版","key":null,"url":"http://naba.51094.com/naba/activity/activity.action?activityId=7&activityType=5&authType=1","subButtons":[]}]}]`

`参数: mpUserName 公众号原始ID`

`返回数据:`

```javascript
{
	"message": "同步成功",
	"success": true
}
```
