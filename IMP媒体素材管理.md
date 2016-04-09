BasePath : http://IP:8080/imp/

1.按类型查询媒体素材列表

接口名：mediaManager/mediaManager!queryMediaList.action

参数： replyType : 媒体素材类型 2:单图文回复 3：多图文回复  mpUserName：公众号原始Id
返回数据
``` javascript 
{
    "data": {
        "resultList": [
            {
                "currentPage": 1,
                "message": null,
                "id": 6,
                "mpUserName": "gh_853df56d4234",
                "title": "imageTextTitle",
                "mediaId": "_Xev9QOZPe9xp-y-rFy5LToiU9tMTCN7o0mBAH36h1Q",
                "author": "testauthor",
                "digest": null,
                "showCoverPic": 1,
                "content": "textcontent哈啊哈",
                "sourceUrl": "testsourceUrl",
                "createTime": "2016-04-05 15:30:01",
                "picUrl": "/usr/local/naba.png",
                "picMediaId": "_Xev9QOZPe9xp-y-rFy5LeDrelzaOvu3DUwHGqRSn0s",
                "mediaUrl": null,
            },
            {
                "currentPage": 1,
                "message": null,
                "id": 5,
                "mpUserName": "gh_853df56d4234",
                "title": null,
                "mediaId": "_GX2Nc8x1lpwcy6xs6RykOIWcyqZ-1GEwT3nXDFnWlJHsjscBRDzDpVQtMhePqO0",
                "author": "author",
                "digest": "digest",
                "showCoverPic": 1,
                "content": "content",
                "sourceUrl": null,
                "createTime": "2016-03-24 14:51:07",
                "picUrl": "",
                "picMediaId": "vIAex41Y8B0UOvPPZXrncxakbOdGrLNO2lbidjQI6BBl6-0EUxT530_KYpUw1W9U",
                "mediaUrl": null,
            }
        ],
        "totalCount": 6
    },
    "success": true
}
```
数据字段说明：
id: 媒体主键序列号 
mpUserName：公众号原始id 
title: 素材标题
mediaId:素材在微信端的媒体id
author:作者
digest:素材描述或者简介
showCoverPic:缩略图是否在正文显示 0：不显示 1：显示 
content:素材正文（富文本）
sourceUrl：素材的原文链接
createTime:创建时间
picUrl：缩略图显示url
picMediaId:缩略图在微信端的id
mediaUrl:整个素材在微信中的浏览地址

2.增加媒体素材

接口名：mediaManager/mediaManager!addMedia.action

参数： 
mediaType : 媒体素材类型 2:单图文 3：多图文
mpUserName：公众号原始Id
content:素材正文内容（富文本）（仅单图文有效）
imageTextTitle: 素材标题（仅单图文有效）
digest：素材描述或着简介（仅单图文有效）
author：素材作者（仅单图文有效）
sourceUrl：素材原文链接（仅单图文有效）
showCoverPic：是否在正文中显示缩略图 0:不显示 1:显示（仅单图文有效）
mediaLogo：File类型 缩略图文件
mediaLogoFileName：缩略图文件名
replyIds：单图文素材id 样例:1,2,3 

返回数据:
{"message":"添加成功","success":true}

3.更新媒体素材
接口名：mediaManager/mediaManager!updateMedia.action
参数：
mediaType : 媒体素材类型 2:单图文回复 3：多图文回复 
更新单图文：
同增加媒体素材
更新多图文：
同增加媒体素材
idx：更新多图文中的第X个素材 从0开始
subMediaId：多图文素材中的子素材主键Id
multiMediaId：多图文素材主键Id
返回数据：
{"message":"更新成功","success":true}

4.删除媒体素材
接口名：mediaManager/mediaManager!delMedia.action
参数：
mediaId：媒体主键id
mediaType : 媒体素材类型 2:单图文回复 3：多图文回复
返回数据：
{"message":"删除成功","success":true}

5.查询素材
接口名：mediaManager/mediaManager!getMediaById.action
参数：
mediaId:媒体素材主键ID
mpUserName: 公众号原始ID
mediaType： 媒体素材类型 2:单图文回复 3：多图文回复

返回数据：
单图文素材：
``` javascript
{
    "data": {
        "id": 6,
        "mpUserName": "gh_853df56d4234",
        "title": "imageTextTitle",
        "mediaId": "_Xev9QOZPe9xp-y-rFy5LToiU9tMTCN7o0mBAH36h1Q",
        "author": "testauthor",
        "digest": null,
        "showCoverPic": 1,
        "content": "textcontent哈啊哈",
        "sourceUrl": "testsourceUrl",
        "createTime": "2016-04-05 15:30:01",
        "picUrl": "/usr/local/naba.png",
        "picMediaId": "_Xev9QOZPe9xp-y-rFy5LeDrelzaOvu3DUwHGqRSn0s",
        "mediaUrl": null

    },
    "success": true
}
```
id: 媒体主键序列号 
mpUserName：公众号原始id 
title: 素材标题
mediaId:素材在微信端的媒体id
author:作者
digest:素材描述或者简介
showCoverPic:缩略图是否在正文显示 0：不显示 1：显示 
content:素材正文（富文本）
sourceUrl：素材的原文链接
createTime:创建时间
picUrl：缩略图显示url
picMediaId:缩略图在微信端的id
mediaUrl:整个素材在微信中的浏览地址

多图文：
``` javascript 
{
    "data": {
        "id": 1,
        "subMediaIds": "4,5,6",
        "subMedias": [
            {
                "id": 4,
                "mpUserName": "gh_853df56d4234",
                "title": null,
                "mediaId": "rORSJmzgtNIXcm7eXyWlyY5Qdsogb89DJRUTFJ_sc9Xuvem6UD21ySZtGK97_4Sl",
                "author": "author",
                "digest": "digest",
                "showCoverPic": 1,
                "content": "content",
                "sourceUrl": null,
                "createTime": "2016-03-24 14:42:40",
                "picUrl": "",
                "picMediaId": "CWxero55obl5bF1iatz18_7BCrqqRKi-IsxrAt4h_fPEke5mWaNLZ9USuPgRegPT",
                "mediaUrl": null,
            }
        ]
    },
    "success": true
}

```
参数说明：
id : 多图文素材主键id
subMediaIds : 子图文id
subMedias : 子图文内容

6.上传素材富文本中的图片
接口名：mediaManager/mediaManager!uploadContentImg.action
参数： 
mpUserName ： 微信原始Id
contentImg : file类型 上传图片
contentImgFileName ：上传图片文件名

返回结果：
{"message":"http://xxxx/xxx.png","success":true}

