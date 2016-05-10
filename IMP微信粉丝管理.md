

BasePath : http://IP:8080/imp/

** 1. 获取粉丝列表 **

`接口名：mpwxuserController!getMpwxuserList.action?currentPage=1&pageSize=20&mpUserName=gh_853df56d4234`

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
		"id": 53, //编号
		"mpUserName": "gh_853df56d4234", 
		"openId": "oFT-8woR-dtB8ONDvggy80J3tP-0",
		"nickName": "张坚楠", //粉丝昵称
		"headImgUrl": "http://wx.qlogo.cn/mmopen/SYeWkon6C6LR5hmiaodEGQkzDdxfnPk0ibcJbvN8BxvuPw6E5CkGIuFVjoMmMPDPo9QtFWdf48ou6W05cXX76Tog/0", //头像
		"subscribe": 1,
		"sex": "男", //性别
		"language": "zh_CN",
		"city": "深圳", //市
		"province": "广东", //省
		"country": "中国", //国家
		"subscribeTime": "2016-01-11 16:36:41", //关注时间
		"unionId": null,
		"sexId": 1,
		"remark": "",
		"groupId": 0,
                "$groupName": "未分组", //组名称
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
		"id": 54,
		"mpUserName": "gh_853df56d4234",
		"openId": "oFT-8wliA23RDK0Zewbo4HtuIv98",
		"nickName": "johnc",
		"headImgUrl": "http://wx.qlogo.cn/mmopen/ajNVdqHZLLAhjv9DpyJiat5jRibEqO76ze5Ds5ZQNiaIAbJWmn7j1LYoW1UGiapdVTkVciaJl3SJVO2GTZcdk4ffvmA/0",
		"subscribe": 1,
		"sex": "男",
		"language": "zh_CN",
		"city": "深圳",
		"province": "广东",
		"country": "中国",
		"subscribeTime": "2016-03-16 16:31:43",
		"unionId": null,
		"sexId": 1,
		"remark": "",
		"groupId": 0,
                "$groupName": "未分组",
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
		"id": 68,
		"mpUserName": "gh_853df56d4234",
		"openId": "oFT-8wqpR8XQZ7SJGfgHzYnd9hcg",
		"nickName": "石头剪刀布",
		"headImgUrl": "http://wx.qlogo.cn/mmopen/l2GFEhvs8zRqj4DTWWUia6nqJ6OjlClUs3PibUI0Kuemu3jVkJQP53zHWlkgCHVTsbeJ5v72vCluoC9OG6Ddib8q4HdHpic1BfZ7/0",
		"subscribe": 1,
		"sex": "女",
		"language": "zh_CN",
		"city": "深圳",
		"province": "广东",
		"country": "中国",
		"subscribeTime": "2016-01-26 14:11:42",
		"unionId": null,
		"sexId": 2,
		"remark": "",
		"groupId": 0,
                "$groupName": "未分组",
		"sortColumnsString": ""
	}],
	"totalCount": 3
}
```
** 2.同步粉丝 **

`接口名：mpwxuserController!refreshMpwxuserList.action?mpUserName=gh_853df56d4234`

`参数: mpUserName 公众号原始ID`

`返回数据:`

```javascript
{
	"message": "同步成功",
	"success": true
}
```

** 3.分组下拉列表 **

`接口名：mpwxgroupController!getGroupName.action?mpUserName=gh_853df56d4234`

`参数: mpUserName 公众号原始ID`

`返回数据:`

```javascript
[{
	"ItemValue": 0,
	"ItemText": "未分组"
},
{
	"ItemValue": 1,
	"ItemText": "黑名单"
},
{
	"ItemValue": 2,
	"ItemText": "星标组"
}]
```

** 4.移动用户到分组 **

`接口名：mpwxgroupController!moveUser2Group.action?mpUserName=gh_853df56d4234&openid_list=['oFT-8wnu0KQ72Z_i3x0WXObtPoqc','oFT-8wq2HlQAYL0SIyhRPpM-mbpQ']&to_groupid=114`

`参数: mpUserName 公众号原始ID openid_list 要移动的粉丝openid list to_groupid 移动到组的ID`

`返回数据:`

```javascript
{
	"message": "",
	"success": true
}
```
