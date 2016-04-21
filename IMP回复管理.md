BasePath : http://IP:8080/imp/

1.查询回复列表

接口名：reply/replyManager!querySubscribeReplyList.action

参数：

mpUserName : 公众号原始id
返回数据
``` javascript
{
    "data": [
        {
            "id": 12, //回复主键id
            "title": "testtitle", //回复标题
            "status": 1, //状态 0 未启用1启用 
            "createTime": 1459841401000,  //创建时间
            "isSubscribe": 1,  //是否是关注回复 1 关注回复 0 普通回复
            "matchType": 1, //匹配类型1:完全匹配2:模糊匹配
            "replyType": 2 //回复类型1:文本回复2:图文回复3:多图文回复
        },
        {
            "id": 9,
            "title": "title",
            "status": 1,
            "createTime": 1458802267000,
            "isSubscribe": 0,
            "matchType": 1,
            "replyType": 2
        }
    ],
    "success": true
}
```

2.增加回复
接口名：reply/replyManager!addReply.action
参数:
mpUserName : 微信公众号原始id

replyType：回复类型1:文本回复2:图文回复3:多图文回复

isUseMaterial ： 是否使用已有素材 0：不使用 1：使用

content ：回复内容 （富文本）

status : 开启状态 0:未开启 1: 开启

title : 回复标题

imageTextTitle : 图文回复标题 (仅单图文回复)

isSubscribe : 是否是关注 0 : 普通回复 1： 关注回复

digest ： 图文回复描述  (仅单图文回复)

matchType ： 匹配类型 1:完全匹配2:模糊匹配 (仅非关注回复)

mediaId：选择已有素材的素材Id （仅isUseMaterial=1时有效）

author : 图文素材的作者 (仅单图文回复)

sourceUrl ： 图文素材的原文链接  (仅单图文回复)

showCoverPic ：正文是否显示缩略图 0：不显示 1：显示 (仅单图文回复)

mediaLogo ： 缩略图文件 File类型 (仅单图文回复)

mediaLogoFileName : 缩略图文件名 (仅单图文回复)

mediaIds ： 多图文素材中的媒体Id(仅多图回复有效)

返回数据:


3.更新回复
接口名：reply/replyManager!updateSubscribeReply.action

参数:

单图文修改同增加回复

多图文修改参数

(1)修改已有多图文回复中的一个图文

idx：被修改的单图文在多图文中的序号

subMediaId：被修改的单图文主键id

multiMediaId:被修改多图文主键id

其它单图文参数同增加单图文回复参数

(2)新增多图文

同增加多图文

返回数据:

4.删除回复

接口名：reply/replyManager!delReply.action

参数：

replyId ： 回复Id

5.获取某个回复的详情

接口名：reply/replyManager!getReplyById.action

参数：

replyId 回复id

返回参数：

``` javascript
{
    "data": {
        "id": 11, //主键序列号
        "matchType": 1, //匹配类型 1:完全匹配2:模糊匹配 (仅非关注回复)
        "keyWord": "testkeyword", // 关键字(仅非关注回复)
        "status": 1, 是否启用 1：启用 0：不启用
        "title": "testtitle", //回复标题
        "replyType": 3, //回复类型1:文本回复2:图文回复3:多图文回复(仅非关注回复)
        "content": null, //回复内容（仅文本回复或者文本关注）
        "mediaId": 1, //回复素材ID
        "isSubscribe": 1 //是否是关注回复 1：关注回复 0：普通回复
    },
    "success": true
}
```

6.上传回复富文本内容的图片

同媒体素材接口中的上传图片接口
