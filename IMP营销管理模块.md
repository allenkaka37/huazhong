BasePath : http://IP:8080/imp/

**1.添加营销活动**
```javascript
接口名称:  activityController!saveActivityInfo.action
参数描述:  
	type			对应活动类型:1-关注,2-注册,3-下载
	name			名字:type=1 公众号名,type =2和3 应用名
	maxmember		参与人数上限
	guideUrl		推广地址:type=1 公众号的关注地址,type=2 注册页面地址
	appType			应用类型:理财,游戏,社交,开发等.英文逗号分隔
	registerType		注册方式:1-手机号,2-邮箱
	sendFlag		是否发送用户记录至第三方.1-发送,0-不发
	sendUrl			第三方的接收消息地址
	shortDescription	下载类的简要描述
	appStoreId		苹果应用商店id
	tencentStore		腾讯应用宝地址
	androidUrl		安卓下载地址
	iosSize			ios版本大小
	androidSize		android版本大小
	icon			应用图标:type=1公众号图标,type=2||3应用图标
	banner			应用横幅:type=3时下载类型的应用banner
	focusBackground		公众号关注类型活动需上传的页面底图
	focusPackage		公众号关注类型活动需上传的礼品包图片
	shareIcon		分享消息中的图标
	shareTitle		分享消息中的标题
	shareDesc		分享消息中的描述
	joinModuleId		参与活动时使用的模板id
	registerExchangeAd	注册兑奖页面广告
	weChatQRCode		公众号的关注二维码
返回数据:
	成功示例:
	{
	"data": {
			id: 20,
			code: null,
			name: "jubaopen45",
			supId: null,
			type: "1",
			status: "1",
			maxmember: 2000,
			price: null,
			guideUrl: null,
			appType: null,
			registerType: null,
			iconUrl: null,
			sendFlag: "0",
			sendUrl: null,
			shortDescription: null,
			appStoreId: null,
			tencentStore: null,
			androidUrl: null,
			iosSize: null,
			androidSize: null,
			banner: null,
			praiseNum: null,
			perateStep: null,
			mustDo: null,
			descritpion: null,
			createDate: "2016-03-04 16:48:12",
			sortColumnsString: "",
			remark:"",
			focusPackage:"",
			focusBackground:"",
			shareIcon:"",
			shareTitle:"",
			shareDesc:""
		},
		"success": true
	}
	异常示例1:
	{
		"message": "保存应用信息失败", 错误信息描述
		"success": false 
	}
	异常示例2:
	{
		"message":"图标上传失败",错误信息描述
		"success":false
	}
```
**1.修改当前用户指定的营销活动**
```javascript
	营销类活动只能在待审核状态下允许修改操作!
接口名称:activityController!updateActivityInfo.action
参数描述:
	id			营销活动的id
	name			名字:关注类活动-公众号名,注册和下载类-应用名
	maxmember		参与人数上限
	guideUrl		推广地址:关注类活动-公众号的关注地址,注册类活动-注册页面地址
	appType			应用类型:理财,游戏,社交,开发等.英文逗号分隔
	registerType		注册方式:1-手机号,2-邮箱
	sendFlag		是否发送用户记录至第三方.1-发送,0-不发
	sendUrl			第三方的接收消息地址
	shortDescription	下载类的简要描述,可做关注类的标题
	appStoreId		苹果应用商店id
	tencentStore		腾讯应用宝地址
	androidUrl		安卓下载地址
	iosSize			ios版本大小
	androidSize		android版本大小
	icon			应用图标:公众号图标或者注册下载类应用图标
	banner			应用横幅:下载类的应用banner
	focusBackground		公众号关注类型活动需上传的页面底图
	focusPackage		共周后关注类型活动需上传的礼品包图片
	shareIcon		分享消息中的图标
	shareTitle		分享消息中的标题
	shareDesc		分享消息中的描述
返回数据:
	成功示例:
	{
	"data": {
			id: 20,
			code: null,
			name: "jubaopen45",
			supId: null,
			type: "1",
			status: "1",
			maxmember: 2000,
			price: null,
			guideUrl: null,
			appType: null,
			registerType: null,
			iconUrl: null,
			sendFlag: "0",
			sendUrl: null,
			shortDescription: null,
			appStoreId: null,
			tencentStore: null,
			androidUrl: null,
			iosSize: null,
			androidSize: null,
			banner: null,
			praiseNum: null,
			perateStep: null,
			mustDo: null,
			descritpion: null,
			createDate: "2016-03-04 16:48:12",
			sortColumnsString: "",
			remark:"",
			focusPackage:"",
			focusBackground:"",
			shareIcon:"",
			shareTitle:"",
			shareDesc:"",
			registerExchangeAd:"",
			weChatQRCode:""
		},
		"success": true
	}
	异常示例1:
	{
		"message": "修改应用信息失败", 错误信息描述
		"success": false 
	}
	异常示例2:
	{
		"message":"图标上传失败", 错误信息描述
		"success":false
	}
	异常示例3:
	{
		"message":"当前状态不允许进行修改操作", 
		"success":false
	}
	异常示例4:
	{
		"message":"应用信息不存在或者您无权操作", 
		"success":false
	}
```

**3.获取当前用户指定的应用信息**
```javascript
接口名称:activityController!getActivityInfo.action
参数描述:
	id			营销活动id
返回数据:
	成功示例:
	{
	"data": {
			id: 20,
			code: null,
			name: "jubaopen45",
			supId: null,
			type: "1",
			status: "1", (1:待审核,	2:审核通过待支付,3:审核不通过,4支出成功已上架,5:已下架)
			maxmember: 2000,
			price: null,
			guideUrl: null,
			appType: null,
			registerType: null,
			iconUrl: null,
			sendFlag: "0",
			sendUrl: null,
			shortDescription: null,
			appStoreId: null,
			tencentStore: null,
			androidUrl: null,
			iosSize: null,
			androidSize: null,
			banner: null,
			praiseNum: null,
			perateStep: null,
			mustDo: null,
			descritpion: null,
			createDate: "2016-03-04 16:48:12",
			sortColumnsString: "",
			remark:"",
			focusPackage:"",
			focusBackground:"",
			shareIcon:"",
			shareTitle:"",
			shareDesc:"",
			priview:""	//预览二维码地址
		},
		"success": true
	}
	异常示例1:
	{
		"message": "应用信息不存在", 错误信息描述
		"success": false 
	}
	异常示例2:
	{
		"message": "获取活动信息失败", 错误信息描述
		"success": false 
	}
```
**4.获取当前用户所有的营销活动**
```javascript
接口地址:activityController!getActivityList.action
参数描述:
	pageSize			每页展示的条数
	currentPage			当前请求的页数
返回数据:
	成功示例1:
	{
		data: {
			resultList: [
				{
					id: 1,
					serviceOrderId: null,
					code: null,
					userId: 1,
					name: "jubaopen",
					supId: null,
					type: "1",
					status: "1",
					maxmember: null,
					price: null,
					guideUrl: null,
					appType: null,
					registerType: null,
					iconUrl: null,
					sendFlag: "0",
					sendUrl: null,
					shortDescription: null,
					appStoreId: null,
					tencentStore: null,
					androidUrl: null,
					iosSize: null,
					androidSize: null,
					banner: null,
					praiseNum: null,
					perateStep: null,
					mustDo: null,
					descritpion: null,
					focusBackground: null,
					focusPackage: null,
					remark: null,
					createDate: null,
					shareIcon:"",
					shareTitle:"",
					shareDesc:"",
					priview:""	//预览二维码地址
				},
				{
					id: 17,
					serviceOrderId: null,
					code: null,
					userId: 1,
					name: "jubaopen12",
					supId: null,
					type: "1",
					status: "1",
					maxmember: null,
					price: null,
					guideUrl: null,
					appType: null,
					registerType: null,
					iconUrl: null,
					sendFlag: "0",
					sendUrl: null,
					shortDescription: null,
					appStoreId: null,
					tencentStore: null,
					androidUrl: null,
					iosSize: null,
					androidSize: null,
					banner: null,
					praiseNum: null,
					perateStep: null,
					mustDo: null,
					descritpion: null,
					focusBackground: null,
					focusPackage: null,
					remark: null,
					createDate: "2016-03-04 16:47:43",
					shareIcon:"",
					shareTitle:"",
					shareDesc:""
					priview:""	//预览二维码地址
				}
			],
			totalCount: 2
		},
		success:true
	}
	成功示例2:
	{
		data: {
			resultList: [ ],
			totalCount: 0
		},
		success: true
	}
	异常示例:
	{
		"message": "获取活动列表失败", 错误信息描述
		"success": false 
	}
```

**5.客户上架营销活动**
```javascript
	只有当营销活动为status=2(审核通过待支付)时,才能执行该动作(支付并上架)
接口名称: activityController!updateActivityShelve.action
参数描述:
	id			营销活动的id
返回数据:
	成功示例:
	{
		"message": "", 
		"success": true 
	}
	异常示例1:
	{
		"message": "该应用信息不存在或者您无权限操作", 错误信息描述
		"success": false 
	}
	异常示例2:
	{
		"message": "当前状态不允许上架操作", 错误信息描述
		"success": false 
	}
	异常示例3:
	{
		"message": "账户中心余额不足,请充值", 错误信息描述
		"success": false 
	}
	异常示例4:
	{
		"message": "应用信息上架失败", 错误信息描述
		"success": false 
	}
```

**6.追加营销活动的上限值**
```javascript
	该动作只允许在应用status=4已上架,或者status=5已结束的状态下进行追加
接口名称: activityController!updateMaxmember.action
参数描述:
	id			营销活动的id
	addNum			追加的人数
返回数据:
	成功示例:
	{
		"message": "", 
		"success": true 
	}
	异常示例1:
	{
		"message": "获取应用信息失败", 错误信息描述
		"success": false 
	}
	异常示例2:
	{
		"message": "该应用信息不存在或者您无权操作", 错误信息描述
		"success": false 
	}
	异常示例3:
	{
		"message": "账户中心余额不足,请充值", 错误信息描述
		"success": false 
	}
	异常示例4:
	{
		"message": "应用追加参与上限失败", 错误信息描述
		"success": false 
	}
```

