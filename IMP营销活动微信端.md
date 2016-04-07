
BasePath : http://IP:PORT/imp

** 1. 获取活动信息,包含该用户的参与记录和活动的奖品信息**

`接口名 : activityClientController!getActivityInfo.action?id=1&openId=lizhijie`

`参数描述 : id -- 活动的id 从页面地址中获取activityId参数值; openId -- 用户的openId 从页面地址中获取openId参数值`

`返回数据 :`
```javascript
	{
	data: {
		id: 37,	//活动的id
		code: "myjf052",	//活动code
		name: "蚂蚁金福",	//活动名字
		type: "3",	//活动类型:1关注,2注册,3下载
		status: "4",	//活动状态 1待审核,2审核通过待支付,3审核不通过,4上架,5下架
		maxmember: 2200,	//活动参与
		guideUrl: null,	//推广地址:关注活动时:为公众号的关注地址,注册活动时:注册页面地址
		appType: "理财",	//应用类型
		registerType: null,	//注册方式:1-手机号,2-邮箱
		iconUrl: null,	//应用图标地址
		shortDescription: null,	//应用的简要描述
		appStoreId: "js3222",	//AppStore应用商店上架ID
		tencentStore: "tmall.com",	//使用应用宝下载使用的地址
		androidUrl: "jd.com",	//安卓版本的下载地址
		iosSize: "17.9",	//IOS版本应用的占用空间大小,单位:M
		androidSize: "20",	//安卓版本应用的占用空间大小,单位:M
		banner: null,	//下载类型详情页面的banner图(目前只支持一张)
		perateStep: null,	//参与步骤,类似于拿吧下载站详情页面的布局
		mustDo: null,	//活动规则,类似于拿吧下载站详情页面的布局
		descritpion: "帮你理财帮你",
		focusBackground: null,	//关注类活动参与页面的背景图
		focusPackage: null,	//关注类活动参与页面的红包图
		createDate: "2016-04-01 14:41:38",	//活动的创建时间
		order: {	//用户的参与状态对象, order=null 则用户为参与
			money: null,	//当活动奖品为随机红包时,该字段为用户得到的现金数,单位:分
			phoneNum: "",	//用户报名使用的手机号
			mail: "",	//用户报名使用的邮箱地址
			status: "1",	//用户的参与状态 1用户已参与，2进行中，3审核未通过、4审核通过待发奖、5已领取
			createDate: "2016-03-14 14:26:41",	//用户的参与时间
			drawDate: null,	//用户领取奖品的时间
			id: 1457936801148,	//用户参与记录的ID,注册类型的活动在跳转至注册页时需传递
			token: "5632c6eece913ab85b04d8d68d8720c9"	
		},
		surprise: {	//活动的奖品对象
			id: 1,	//奖品ID
			name: "sur_test",	//奖品名称
			title: "活动礼包",	//奖品title
			description: "完成活动领取奖励",	//奖品描述
			imgUrl: null,	//奖品的图片地址
			type: "2",	//奖品的类型 1:流量直充.2:定额红包.3:随机红包
			cash: 100,	//定额红包的现金数或随机红包的基数
			stochastic: 0,	//随机红包的附加值,此时随机红包的区间为 A~A+B
			ltPackage: "",	//联通号码充值流量数
			dxPackage: "",	//点好号码充值流量数
			ydPackage: ""	//移动号码充值流量数
		},
		joinNum: 1,	//该活动目前的参与人数
		drawNum: 0,	//该活动目前的领奖人数
		praiseNum: 0,	//该活动目前的点赞人数
		isPraise: 0,	//该用户是否点赞
		shareIcon: "upload/shareIcon/20160401144138602417.png",	//分享图标
		shareTitle: "很好的产品哦",	//分享标题
		shareDesc: "为什么呢"	//分享描述
	},
	success: true
	}
```

** 2. 用户参与某个活动**

`接口名 : activityClientController!joinActivity.action?id=1&openId=lizhijie&phoneNum=13560792616&mail=`

`参数描述 : id -- 活动的id 从页面地址中获取activityId参数值; openId -- 用户的openId 从页面地址中获取openId参数值; phoneNum -- 用户输入的手机号; mail -- 用户输入的邮箱地址`


`返回数据 :`
```javascript
	{
	data: {
		money: null,	
		phoneNum: "",	//用户输入的手机号
		mail: "",	//用户输入的邮箱地址
		status: "1",	//用户的参与状态  1用户已参与，2进行中，3审核未通过、4审核通过待发奖、5已领取
		createDate: "2016-03-14 14:26:41",	//用户的参与时间
		drawDate: null,	//用户的领奖时间
		id: 1457936801148,	//用户参与记录的ID
		token: "5632c6eece913ab85b04d8d68d8720c9"	//用户参与记录独有token
	},
	success: true
	}
```

** 3. 兑换奖品接口**

`接口名 : activityClientController!exchageForFocus.action?id=1&openId=lizhijie`

`参数描述 : id -- 活动的id 从页面地址中获取activityId参数值; openId -- 用户的openId 从页面地址中获取openId参数值`

`返回数据 :`
```javascript
	{
	data: {
		money: null,	
		phoneNum: "",	//用户输入的手机号
		mail: "",	//用户输入的邮箱地址
		status: "5",	//用户的参与状态  1用户已参与，2进行中，3审核未通过、4审核通过待发奖、5已领取
		createDate: "2016-03-14 14:26:41",	//用户的参与时间
		drawDate: null,	//用户的领奖时间
		id: 1457936801148,	//用户参与记录的ID
		token: "5632c6eece913ab85b04d8d68d8720c9"	//用户参与记录独有token
	},
	success: true
	}
```

** 4. 用户为某个活动点赞**
`一个用户只允许对一个活动进行一次点赞,如果获取应用详情时返回用户已赞,则页面上屏蔽点赞功能`

`接口名 : activityClientController!clickPraise.action?id=1&openId=lizhijie`

`参数描述 : id -- 活动的id 从页面地址中获取activityId参数值; openId -- 用户的openId 从页面地址中获取openId参数值`

`返回数据 :`
```javascript
	{
	message: "",
	success: true
	}
```

