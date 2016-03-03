

BasePath : http://IP:8080/huazhong/

**1.获取用户对应的公司信息**

`接口名：companyController!getCompanyInfo.action`

`参数： 无`

`返回数据：`
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
		"companyName": "华众时代",
		"companyLogo": "",
		"licensePic": "",
		"address": "广州市",
		"contacts": "MM",
		"phone": "7758521",
		"email": "11@qq.com",
		"userId": 1,
		"sortColumnsString": ""
	},
	"success": true
}

{
	"message": "没有该用户的公司信息",
	"success": false
}
```
**2.添加公司信息**

`接口名：companyController!saveCompanyInfo.action?companyName=华众时代&address=深圳市&contacts=美女&phone=7758521&email=11@qq.com`

`参数: companyName 公司名称 address 公司地址 contacts 公司联系人 phone 公司联系电话 email 公司邮箱 companyLogo 公司Logo licensePic 营业执照`

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

**3.修改公司信息**

`接口名：companyController!updateCompanyInfo.action?id=1&address=广州市&contacts=MM`

`参数：address 公司地址 contacts 公司联系人 *** 参数参考新增公司信息`

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
		"companyName": "华众时代",
		"companyLogo": "",
		"licensePic": "",
		"address": "广州市",
		"contacts": "MM",
		"phone": "7758521",
		"email": "11@qq.com",
		"userId": 1,
		"sortColumnsString": ""
	},
	"success": true
}
```
