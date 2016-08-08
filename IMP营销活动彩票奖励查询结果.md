
BasePath : http://IP:PORT/imp


** 1. 获取微信用户拥有的彩票信息**

`接口名 : lotteryController!getLotteryInfoList.action?openId=oFT-8wsyXIfLxAQdPmIn5OfInuZU&currentPage=1

`参数描述 : openId -- 用户的openId 从页面地址中获取openId参数值`
			currentPage -- 获取的页数, 从1开始

`返回数据 :`
```javascript
	{
		data: {
			result: [
				{
				gameCode: "201",		//彩票类型 201 双色球
				issue: "2016082",		//彩票期号
				amount: "20",			//购买的彩票金额 单位分
				grade: null,			//奖等
				prize: null,			//奖金
				status: "2",			//状态,0失败；1未开奖；2未中奖，3已中奖，4已兑奖，5中大奖，6已发奖
				voteNums: "03/06/13/15/22/24//02",		//彩票号码
				multi: "1",				//倍数
				lotteryNums: "17/24/25/16/32/01//14",		//开奖号码
				specialNum: "",			//特殊号码
				orderId: "1466417741824"		//订单号
				},
				{
				gameCode: "201",
				issue: "2016082",
				amount: "20",
				grade: "6",
				prize: "50",
				status: "4",
				voteNums: "02/07/14/16/17/31//01",
				multi: "1",
				lotteryNums: "17/24/25/16/32/01//14",
				specialNum: "",
				orderId: "20"
				},
				{
				gameCode: "201",
				issue: "2016082",
				amount: "20",
				grade: "6",
				prize: "50",
				status: "4",
				voteNums: "02/07/14/16/17/31//01",
				multi: "1",
				lotteryNums: "17/24/25/16/32/01//14",
				specialNum: "",
				orderId: "50"
				}
			],
			size: 3
			},
			success: true
		}						
```

** 2. 获取用户个人基础信息**
`接口名 : lotteryController!getUserInfo.action?openId=oFT-8wsyXIfLxAQdPmIn5OfInuZU

`参数描述 : openId -- 用户的openId 从页面地址中获取openId参数值`
 
`返回数据 :`
```javascript
	{
		data: {
			openId: "oFT-8wht6NU7GXq08VHOiCxKEQiA",
			mobile: "13560792616",		//用户手机号码
			cardId: "410823198908220195",	// 用户身份证号码
			name: "李志杰",		//用户真实姓名
			bankCardNo: "110",	//用户银行卡号
			bankName: "110",	//银行卡号开户行
			bankBranchName: "110"	//银行卡开户行支行
		},
		success: true
	}										
```

** 3. 设置用户个人基础信息**
`接口名 : lotteryController!setUserInfo.action?openId=oFT-8wsyXIfLxAQdPmIn5OfInuZU&mobile=13560792616&cardId=410823198908220195&name=李志杰&bankCardNo=110&bankName=110&bankBranchName=110`

`参数描述 : 参考获取用户个人信息返回字段`
 
`返回数据 :`
```javascript
	//失败情况
	{
		message: "银行卡码已被其他用户绑定,请更换!",
		success: false
	}

	//成功情况
	{
		message: "",
		success: true
	}	
```

**4. 用户提取**

`接口名 : lotteryController!enCash.action?openId=&orderId=`
`参数描述 : openId -- 用户的openId 从页面地址中获取openId参数值`
	   `orderId 订单号`
`返回数据 :`
```javascript
	//失败情况
	{
		message: "",
		success: false
	}

	//成功情况
	{
		message: "",
		success: true
	}	
```

