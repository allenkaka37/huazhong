

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
		"$eq_accountId": null,
		"$payStatus": "支付成功",
		"$isRecharge": "消费",
		"$serviceType": "短信",
		"id": 2,
		"payStatus": 1,
		"createTime": "2016-03-08 11:14:49",
		"payTime": "2016-03-08 11:14:49",
		"accountId": 1,
		"isRecharge": 0,
		"serviceId": null,
		"serviceType": 2,
		"serialNumber": "1457406889",
		"price": 90.0,
		"amount": null,
		"summary": "购买短信",
		"alipayTradeNo": null,
		"alipayBuyerEmail": null,
		"sortColumnsString": ""
	},
	{
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
		"$eq_accountId": null,
		"$payStatus": "支付成功",
		"$isRecharge": "充值",
		"$serviceType": null,
		"id": 10,
		"payStatus": 1,
		"createTime": "2016-03-18 15:31:57",
		"payTime": "2016-03-18 15:33:09",
		"accountId": 1,
		"isRecharge": 1,
		"serviceId": null,
		"serviceType": null,
		"serialNumber": "1458286316",
		"price": 0.01,
		"amount": null,
		"summary": "充值",
		"alipayTradeNo": "2016031821001004870279853794",
		"alipayBuyerEmail": "15986793724",
		"sortColumnsString": ""
	}],
	"totalCount": 2
}
```
