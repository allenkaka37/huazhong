

BasePath : http://IP:8080/imp/

** 1. 获取分组列表 **

`接口名：mpwxgroupController!getMpwxgroupList.action?currentPage=1&pageSize=20&mpUserName=gh_853df56d4234`

`参数： currentPage 当前页码 pageSize 每页数量 mpUserName 公众号原始ID`

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
		"$eq_mpUserName": null,
		"$eq_groupId": null,
		"$like_nickName": null,
		"id": 0, //编号
		"mpUserName": "gh_853df56d4234",
		"name": "未分组", //组名称
		"count": 16, //粉丝量
		"summary": null, //简介
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
		"$eq_mpUserName": null,
		"$eq_groupId": null,
		"$like_nickName": null,
		"id": 1,
		"mpUserName": "gh_853df56d4234",
		"name": "黑名单",
		"count": 0,
		"summary": null,
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
		"$eq_mpUserName": null,
		"$eq_groupId": null,
		"$like_nickName": null,
		"id": 2,
		"mpUserName": "gh_853df56d4234",
		"name": "星标组",
		"count": 0,
		"summary": null,
		"sortColumnsString": ""
	}],
	"totalCount": 3
}
```
** 2.同步分组 **

`接口名：mpwxgroupController!refreshMpwxgroupList.action?mpUserName=gh_853df56d4234`

`参数: mpUserName 公众号原始ID`

`返回数据:`

```javascript
{
	"message": "同步成功",
	"success": true
}
```

** 3.保存/更新分组 **

`接口名：mpwxgroupController!doSave.action?mpUserName=gh_853df56d4234&name=rongsheng&summary=sdkfjdsklfj&id=102`

`参数: mpUserName 公众号原始ID name 组名称 summary 简介 id(可选参数) 组ID（有该参数表示修改，没该参数表示新增）`

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
		"$eq_mpUserName": null,
		"$eq_groupId": null,
		"$like_nickName": null,
		"id": 114,
		"mpUserName": "gh_853df56d4234",
		"name": "rongsheng",
		"count": null,
		"summary": "sdkfjdsklfj",
		"sortColumnsString": ""
	},
	"success": true
}
```
