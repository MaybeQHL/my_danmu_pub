# my_danmu_pub
免费、公开、快速的弹幕系统API。

## 初衷
服务于类似樱花动漫类型的网站、app。

## 公告
目前系统处于`测试`阶段,可能会修改相关的逻辑。

## 提示
切勿使用本系统做违法乱纪的事情，一切后果自己承担。

## 弹幕演示
[在线演示](http://null_639_5368.gitee.io/my_danmu )

## 文档
> 对接原则建立在异步的情况下,如果系统出问题至少你要保证你原来的逻辑不受影响，顶多就是没有弹幕。

API根地址: https://api.danmu.oyyds.top

[API对接文档](https://console-docs.apipost.cn/doc.html?url=508e9181d81a978c&salt=d92a27922cea066a#b9ce2fcf-2f24-4f5c-8b93-c82254714851)

### 对接顺序(具体细节请查看API对接文档)
 #### 查询资源（视频）id (如果无资源可自行添加)
 api: https://api.danmu.oyyds.top/api/goods/getSome?name=斗破

 #### 查询集id (如果无集可自行添加)
 api: https://api.danmu.oyyds.top/api/episode/getOneByNumer?number=1-0&goodsId=624694e360f855ce59c6b1c6
 
**这里number对应的规则 -> 预告：`0-1`,`0-2` 正片: `1-0`(第一集),`2-0`(第二集)**

 #### 查询、添加弹幕 
 查询弹幕api: https://api.danmu.oyyds.top/api/message/getSome?episodeId=62469a52560d76ba26d7dafb
 
 添加弹幕api: https://api.danmu.oyyds.top/api/message/addOne
 
### HTTP响应结构
```
{
 code:200， // 200 正常 500 错误 
 msg：'',   // 提示信息
 data:[]    // 数据
}
```

### 弹幕功能
1. 纯文本类型弹幕
2. 弹幕类型有头部、底部、滚动、魔法弹幕(暂未实现).

## 限制

1. 同一IP限制10秒内请求最多5次。
2. 系统会对敏感词进行检查。

## 捐赠

本系统开发、部署、维护都是作者自己出钱、出力，如果有兴趣赞助联系本人，邮箱地址:`maybe52052@gmail.com`
## 交流群
群1：262687084

# Changelog

## 2022-04-08
### 🎁Added
- 添加资源类型字段
- 添加首页
### 🤝Changed
### 🐛Fixed

## 2022-04-07
### 🎁Added
- 增强敏感词过滤
### 🤝Changed
- 优化了验证敏感词的逻辑
### 🐛Fixed
