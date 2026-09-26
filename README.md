# openwrt-srun-watchdog
由于项目中使用的部分移动机器人、无人机等智能体（Agent）无法独立完成校园网的 Portal 网页认证，因此开发了基于 OpenWrt 的自动认证与网络共享方案。通过路由器运行 SRun 自动认证程序，实现校园网自动登录，并利用 NAT 为局域网内的多台设备提供网络连接。
本项目是基于https://github.com/vidar-team/srun-login 开源的认证程序，续写了一个实时检测自动认证的脚本
1. 文件安装位置

## 文件安装位置

| 文件名称 | OpenWrt 安装路径 | 用途 |
|---|---|---|
| srun | /etc/init.d/srun | 开机自启动服务 |
| srun-watchdog | /usr/bin/srun-watchdog | 自动检测网络 |
| srun.conf | /etc/srun.conf | 保存账号密码 |
| srun-login | /root/srun-login | 校园网认证程序 |

其中srun-login 由vidar-team开发，而 srun.conf 为账号密码配置，自行填写

