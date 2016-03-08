

BasePath : http://IP:8080/imp/

**1.短信充值**

`接口名：SMScontroller!purchaseSMS.action?amount=1000`

`参数： amount 购买的短信条数`

`返回数据：`
```javascript
{
	"data": {
		"sucess": true,
		"serialNumber": "1457406889"
	},
	"success": true
}

{
	"data": {
		"message": "扣款余额不足",
		"sucess": false,
		"serialNumber": "0"
	},
	"success": false
}
```
**2.发送短信**

`接口名：SMScontroller!sendSMS.action?content=三三四四嗖嗖嗖&phoneNums=15986793724,13480117676`

`参数: phoneNums 电话号码（多个中间用英文逗号隔开） content 短信内容`

`返回数据:`

```javascript
{
	"message": "发送成功",
	"success": true
}

{
	"message": "发送失败",
	"success": false
}
```

**3.获得短信发送记录列表**

`接口名：SMScontroller!getSMSRecords.action?currentPage=1&pageSize=20`

`参数：currentPage 当前页码 pageSize 每页记录条数`

`返回数据:`

```javascript
{
	"resultList": [{
		"pageSize": 20,
		"currentPage": 1,
		"topCount": null,
		"sortColumns": null,
		"cmd": null,
		"queryDynamicConditions": {
			
		},
		"sortedConditions": {
			
		},
		"dynamicProperties": {
			
		},
		"success": null,
		"message": null,
		"id": 2,
		"phoneNums": "15986793724,13480117676",
		"content": "三三四四嗖嗖嗖",
		"countNum": 2,
		"smsCost": 0.18,
		"accountId": 1,
		"createTime": "2016-03-08 11:23:50",
		"sortColumnsString": ""
	}],
	"totalCount": 1
}
```
