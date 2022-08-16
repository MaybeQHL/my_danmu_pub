
# my_danmu_pub
![20684083](https://user-images.githubusercontent.com/34638673/163958311-65404541-49b1-4840-8a19-4b7f46207e9b.gif)

免费、公开、快速的弹幕系统API。

## 初衷
服务于类似樱花动漫类型的网站、app。

## 公告
目前系统处于`测试`阶段,可能会修改相关的逻辑。

**正在开发新的分块接口系统可能不稳定，请见谅。**

## 提示
![2069726C](https://user-images.githubusercontent.com/34638673/163958548-d098391d-a54a-4621-aacb-13a5c3d5f6f3.jpg)

- 切勿使用本系统做违法乱纪的事情，一切后果自己承担。
- 切勿恶意占用服务器资源（如恶意添加资源、恶意发送弹幕、恶意流量攻击）,一经发现永久冻结ip。
## 弹幕演示
[在线演示](http://null_639_5368.gitee.io/my_danmu )


## 平台弹幕优先级（只取一个平台弹幕）
1. B站
2. **腾讯视频 （腾讯视频目前采用片段获取弹幕，所以分块接口正在开发中...尽情期待）**


## 文档
> 对接原则建立在异步的情况下,如果系统出问题至少你要保证你原来的逻辑不受影响，顶多就是没有弹幕。

API根地址: https://api.danmu.oyyds.top

对接请看这里：
[API对接文档](https://console-docs.apipost.cn/doc.html?url=508e9181d81a978c&salt=d92a27922cea066a#b9ce2fcf-2f24-4f5c-8b93-c82254714851)

### 对接顺序(具体细节请查看API对接文档)

 #### 查询、添加弹幕
 
 查询弹幕api v1: https://api.danmu.oyyds.top/api/message/getSome?name=斗破苍穹第一季&number=第01集&type=1
 
 查询弹幕api v2: https://api.danmu.oyyds.top/api/message/getSomeV2?name=斗罗大陆&number=第01集&type=1&flag=0&duration=1440
  
 > 备注: 如果没有该资源会自动添加
 
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
3. 单集弹幕最大6000条(暂时)

## 捐赠

本系统开发、部署、维护都是作者自己出钱、出力，如果有兴趣赞助联系本人，邮箱地址:`maybe52052@gmail.com`
## 交流群
discord: https://discord.gg/qXEb2Hcr
群1：262687084

# Changelog


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
