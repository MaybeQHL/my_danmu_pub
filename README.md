# my_danmu_pub
免费、公开、快速的弹幕系统API。

## 初衷
服务于类似樱花动漫类型的网站、app。

## 公告
目前系统处于`测试`阶段,可能会修改相关的逻辑。

## 提示
切勿使用本系统做违法乱纪的事情，一切后果自己承担。

## 文档
> 对接原则建立在异步的情况下,如果系统出问题至少你要保证你原来的逻辑不受影响，顶多就是没有弹幕。

API根地址: `https://api.danmu.oyyds.top`

[API对接文档](https://console-docs.apipost.cn/doc.html?url=508e9181d81a978c&salt=d92a27922cea066a#b9ce2fcf-2f24-4f5c-8b93-c82254714851)

### 对接顺序
1. 查询资源（视频）id `https://api.danmu.oyyds.top/api/goods/getSome?name=斗破
`，如果无可以自行添加
2. 查询集id  `https://api.danmu.oyyds.top/api/episode/getOneByNumer?number=1-0&goodsId=624694e360f855ce59c6b1c6`, 如果无可以自行添加
3. 查询、添加弹幕 `message相关`
### 响应
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

1. 同一IP限制5秒请求一次。
2. 对弹幕进行关键词过滤（暂未实现）

## 捐赠

本系统开发、部署、维护都是作者自己出钱、出力，如果有兴趣赞助联系本人，邮箱地址:`maybe52052@gmail.com`
