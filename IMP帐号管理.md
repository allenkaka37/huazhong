

BasePath : http://IP:8080/imp/

**1.帐号充值**

`接口名：alipayController!accountRecharge.action?WIDtotal_fee=188`

`参数： WIDtotal_fee 充值金额`

`返回数据：`
```javascript

```
**2.获取当前用户的帐号信息**

`接口名：accountController!getAccountInfo.action`

`参数: 无`

`返回数据:`

```javascript
{
	"data": {
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
		"id": 1,
		"balance": 0.0,
		"invalidTime": null,
		"userId": 1,
		"smsBalance": 0,
		"sortColumnsString": ""
	},
	"success": true
}
```

**3.获取当前用户的订单信息**

`接口名：accountController!getOrderList.action?currentPage=1&pageSize=20`

`参数：currentPage 当前页码 pageSize 每页数量`

`返回数据:`

```javascript
{
	"data": [{
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
		"id": 1,
		"payStatus": 1,
		"createTime": "2016-03-05 14:44:35",
		"payTime": null,
		"accountId": 1,
		"isRecharge": 1,
		"serviceId": null,
		"serviceType": null,
		"serialNumber": "1457160274",  流水号
		"price": 0.01,
		"amount": null,
		"summary": "充值",
		"alipayTradeNo": null,
		"alipayBuyerEmail": null,
		"sortColumnsString": ""
	}],
	"success": true
}
```
