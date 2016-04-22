BasePath : http://IP:8080/imp/

** 1. 获取微信菜单信息 **

`接口名：dataStatisticController!getDataStatisticList.action?mpUserName=gh_853df56d4234&startTime=2016-04-16&endTime=2016-04-21`

`参数： mpUserName 公众号原始ID startTime 开始时间 endTime 结束时间`

`返回数据：`
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
		"$ge_refDate": null,
		"$le_refDate": null,
		"$eq_mpUserName": null,
		"id": 3,
		"mpUserName": "gh_853df56d4234",
		"refDate": "2016-04-19",
		"newUser": 0,
		"cancelUser": 0,
		"cumulateUser": 19,
		"intPageReadUser": 1,
		"intPageReadCount": 3,
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
		"$ge_refDate": null,
		"$le_refDate": null,
		"$eq_mpUserName": null,
		"id": 4,
		"mpUserName": "gh_853df56d4234",
		"refDate": "2016-04-20",
		"newUser": 0,
		"cancelUser": 0,
		"cumulateUser": 19,
		"intPageReadUser": 3,
		"intPageReadCount": 22,
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
		"$ge_refDate": null,
		"$le_refDate": null,
		"$eq_mpUserName": null,
		"id": 2,
		"mpUserName": "gh_853df56d4234",
		"refDate": "2016-04-21",
		"newUser": 0,
		"cancelUser": 0,
		"cumulateUser": 19,
		"intPageReadUser": 1,
		"intPageReadCount": 1,
		"sortColumnsString": ""
	}],
	"totalCount": 3
}
```
