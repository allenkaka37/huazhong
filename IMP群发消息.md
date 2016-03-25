

BasePath : http://IP:8080/imp/

** 1. 获取群发消息列表 **

`接口名：massmessageController!getMassmessageList.action?currentPage=1&pageSize=20&mpUserName=gh_853df56d4234`

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
		"id": 1,
		"mpUserName": "gh_853df56d4234",
		"title": "发送标题", //标题
		"type": 1, //消息类型
		"sendMode": 3, //群发方式
		"createTime": "2016-03-25 16:23:31", //发送时间
		"status": 1, //群发状态
		"mediaId": null, //素材ID
		"content": "就开始地方看见看", //文本内容
		"groupIds": null, //微信组ID
		"openIds": null, //粉丝openId
		"sortColumnsString": ""
	}],
	"totalCount": 1
}
```
** 2. 群发消息 **

`接口名：massmessageController!sendMessage.action?mpUserName=gh_853df56d4234&title=发送标题&type=1&sendMode=3&content=就开始地方看见看&mediaId=rORSJmzgtNIXcm7eXyWlyY5Qdsogb89DJRUTFJ_sc9Xuvem6UD21ySZtGK97_4Sl&groupIds=0,1&openIds=ssdjfksdkfj,sddkjfksdj`

`参数: mpUserName 公众号原始ID|title 标题|type 消息类型 1:文本;2:图文;3:多图文|sendMode 群发方式 1:分组群发;2:指定粉丝;3:全部粉丝|mediaId 素材ID|groupIds 微信组ID, 多个中间用英文逗号隔开|openIds 粉丝openId（要求大于2，小于10000，中间英文逗号隔开）`

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
		"id": 1,
		"mpUserName": "gh_853df56d4234",
		"title": "发送标题",
		"type": 1,
		"sendMode": 3,
		"createTime": "2016-03-25 16:23:31",
		"status": 1,
		"mediaId": null,
		"content": "就开始地方看见看",
		"groupIds": null,
		"openIds": null,
		"sortColumnsString": ""
	},
	"success": true
}
```
