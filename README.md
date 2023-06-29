小白部署手册https://nb.adone.eu.org/article/edgetunnel

这是一个名为 edgetunnel 的 github 项目，可以通过 Cloudflare Workers 部署一个 vless协议的 V2ray代理。
提醒各位，本项目仅限技术交流使用，请勿滥用，由此引起的账号封禁等风险后果自负。
项目地址
https://github.com/zizifn/edgetunnel
部署教程
1、访问 https://dash.cloudflare.com/login 注册并登录账号，点击 Workers 和 Pages ，点击 创建应用程序 
notion image
notion image
notion image
2、打开项目的.js文件 https://github.com/zizifn/edgetunnel/blob/main/src/worker-vless.js 全选复制里面的代码
notion image
3、Ctrl+V 粘贴到 Workers 编辑器
notion image
4、修改 UUID 和 proxyIP，UUID 可选择在线生成 https://1024tools.com/uuid 复制粘贴，这里提供一个IP let proxyIP = ‘103.200.112.108’; 同样复制粘贴，最后点击保存并部署 
notion image
5、添加自定义域名，访问（你绑定的自定义域名+/你的UUID)生成 V2ray 配置链接 
notion image
notion image
6、将复制的V2ray 配置链接粘贴到 V2rayN 客户端，地址填入优选IP ，即可成功科学上网。优选IP 可通过 https://stock.hostmonit.com/CloudFlareYes 获取，或者加入TG群 https://t.me/CF_NAT
notion image
 
提醒各位
本项目仅限技术交流使用，请勿滥用，由此引起的账号封禁等风险自负。
 
有些小伙伴可能没有域名，其实不用自定义域名也是可以的，客户端里去掉tls加密，端口改为80或者2052即可。
教程第4步完成部署之后，可以
notion image
 
配置示例：
notion image
