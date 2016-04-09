
BasePath : http://IP:8080/imp/

1.获取公众号列表

接口名：mpInfoManager/mpInfoManager!queryMpInfoList.action

参数： 无

返回数据：
```javascript
{
    "data": {
        "resultList": [
            {
                "id": 24,
                "appId": null,
                "nickName": "HSTimesTest",
                "headImg": "http://wx.qlogo.cn/mmopen/fAjl32tMuq2Hh75VpRnIn01PcJ3o598CMCru8BmwV8FFD12Vf4icyrfTrLgN1xL30xibkZiavYA1br9Kmpia9gUj1OHSfZ04MmnW/0",
                "serviceType": null,
                "verifyType": null,
                "userName": "gh_853df56d4234",
                "qrcodeUrl": null
            },
            {
                "id": 23,
                "appId": null,
                "nickName": "HSTimesTest",
                "headImg": "http://wx.qlogo.cn/mmopen/fAjl32tMuq2Hh75VpRnIn01PcJ3o598CMCru8BmwV8FFD12Vf4icyrfTrLgN1xL30xibkZiavYA1br9Kmpia9gUj1OHSfZ04MmnW/0",
                "serviceType": null,
                "verifyType": null,
                "userName": "gh_853df56d4234",
                "qrcodeUrl": null
            }
        ],
        "totalCount": 15
    },
    "success": true
}
```
数据字段含义 resultList ： 数据列表 totalCount ：查询总数
id ：主键 nickName ： 公众号昵称 headImg ： 公众号头像 mpUserName ： 公众号原始id

2.获取公众号信息
接口名：mpInfoManager/mpInfoManager!getMpInfo.action
参数： mpinfoId 公众号托管id 

返回数据：
```javascript
{
    "data": {
        "id": 9,
        "appId": "wxce667fae30580d88",
        "nickName": "HSTimesTest",
        "headImg": "http://wx.qlogo.cn/mmopen/fAjl32tMuq2Hh75VpRnIn01PcJ3o598CMCru8BmwV8FFD12Vf4icyrfTrLgN1xL30xibkZiavYA1br9Kmpia9gUj1OHSfZ04MmnW/0",
        "serviceType": "服务号",
        "verifyType": "微信认证",
        "userName": "gh_853df56d4234",
        "qrcodeUrl": null
    },
    "success": true
}
```
数据字段含义
id ：主键 appId ：微信号 nickName ：公众号昵称 headImg ：公众号头像  serviceType： 公众号服务类型 订阅号 服务号 verifyType： 微信认证 
userName ：微信原始Id qrcodeUrl :二维码url

3.删除公众号信息
接口名：mpInfoManager/mpInfoManager!delMpInfo.action
参数： mpinfoId 公众号托管id 
返回数据：
```javascript
{"message":"删除成功","success":true}
```
