

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
	"message": "",
	"success": true
}

{
	"message": "该公司名称已经存在",
	"success": false
}
```

**3.获取当前用户的订单信息**

`接口名：accountController!getOrderList.action`

`参数：无`

`返回数据:`

```javascript

```
