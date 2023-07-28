# my_danmu_pub

<p align="center"><img src="https://user-images.githubusercontent.com/34638673/163958311-65404541-49b1-4840-8a19-4b7f46207e9b.gif" width=150 height=150 /></p>

<p align="center">免费、公开、快速的弹幕系统API</p>


## 初衷
服务于类似樱花动漫类型的网站、app。

## 公告

<h1>项目由于没有设置权限被居心叵测的人滥用导致被各种平台封禁，即日起该项目暂时开放。</h1>

## 已对接的项目

_如果你的项目用到了本系统,可以提pr进行一个展示。_

[媒体盒子(MediaBox)](https://github.com/RyensX/MediaBox)

## 友情提示

- 切勿使用本系统做违法乱纪的事情，一切后果自己承担。
- 切勿恶意占用服务器资源（如恶意添加资源、恶意发送弹幕、恶意流量攻击）,一经发现永久冻结ip。

## 弹幕演示
[在线演示](http://null_639_5368.gitee.io/my_danmu )

## 文档
> 对接原则建立在异步的情况下,如果系统出问题至少你要保证你原来的逻辑不受影响，顶多就是没有弹幕。

API根地址: https://api.danmu.oyyds.top

对接请看这里：
[API对接文档](https://console-docs.apipost.cn/doc.html?url=508e9181d81a978c&salt=d92a27922cea066a#b9ce2fcf-2f24-4f5c-8b93-c82254714851)
 
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
3. 单集弹幕最大6000条(暂时)

## 捐赠

本系统开发、部署、维护都是作者自己出钱、出力，如果有兴趣赞助联系本人，邮箱地址:`maybe52052@gmail.com`
## 交流群

discord: https://discord.gg/sHNpPzrurp

群1：262687084

# Changelog

## 2023-03-12
### 🎁Added
- 编写弹幕数量优化算法以保证不会有海量的弹幕数据返回给客户端（太多的数据会加重http传送负担和客户端压力）
### 🤝Changed
- 对查询速度进行了几何倍数的优化
### 🐛Fixed


## 2022-09-30
### 🎁Added
### 🤝Changed
### 🐛Fixed
- 修复dandan弹幕颜色解析错误的问题


## 2022-09-07
### 🎁Added
### 🤝Changed
### 🐛Fixed
- 修复dandan弹幕服务器无法连接的问题


## 2022-09-06
### 🎁Added
### 🤝Changed
### 🐛Fixed
- 修复B站番剧搜索api的bug

## 2022-08-30
### 🎁Added
- 缓存人人剧集详情，加快查询速度
### 🤝Changed
### 🐛Fixed

## 2022-08-27
### 🎁Added
- 对接人人弹幕
- 优化人人弹幕
### 🤝Changed
### 🐛Fixed

## 2022-08-18
### 🎁Added
- 对接弹弹弹幕
### 🤝Changed
### 🐛Fixed


## 2022-08-17
### 🎁Added
- 查询弹幕v3（自定义平台整集弹幕）
### 🤝Changed
### 🐛Fixed

## 2022-08-14
### 🎁Added
- 公测查询弹幕v2（片段弹幕）
### 🤝Changed
### 🐛Fixed
## 2022-08-10
### 🎁Added
- 对接腾讯弹幕
### 🤝Changed
### 🐛Fixed


## 2022-06-07
### 🎁Added
### 🤝Changed
### 🐛Fixed
- 修复bilibili弹幕颜色显示不正确的bug

## 2022-06-03
### 🎁Added
- 对接bilibili国内弹幕
### 🤝Changed
- 更改系统逻辑
### 🐛Fixed

## 2022-04-18
### 🎁Added
- 添加访问黑名单
### 🤝Changed
- 更改系统逻辑
### 🐛Fixed

## 2022-04-09
### 🎁Added
- 限制单集弹幕最大6000条(暂时)
### 🤝Changed
- 对弹幕查询速度进行了优化
### 🐛Fixed

## 2022-04-08
### 🎁Added
- 添加资源类型字段
- 添加首页
### 🤝Changed
### 🐛Fixed
- 数据库时区问题

## 2022-04-07
### 🎁Added
- 增强敏感词过滤
### 🤝Changed
- 优化了验证敏感词的逻辑
### 🐛Fixed
