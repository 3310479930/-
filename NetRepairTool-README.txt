网络修复工具说明
================

文件：NetRepairTool.exe

界面：
- 类似安全软件网络修复页的清单式界面。
- 点击“全面检查”后，会逐项显示“检查中 / 正常 / 异常”。
- 检查结束后会显示“一键修复”或“仍要修复”。
- 点击“查看日志”可以看到每一步检测和修复流程。

检查项目：
- 网络硬件配置：检查网卡是否存在、是否启用
- 网络连接配置：检查有效 IPv4 和网关
- DHCP服务：检查 DHCP Client 服务
- DNS服务：检查 DNS Client 服务
- HOSTS文件：检查 HOSTS 自定义重定向
- LSP协议：检查 Winsock 目录
- IE代理：检查 WinHTTP 代理配置
- 环境变量：检查系统 Path 是否可读取

修复动作：
- ipconfig /flushdns
- netsh winsock reset
- netsh int ip reset
- arp -d *
- ipconfig /release
- ipconfig /renew

注意：
- 程序需要管理员权限，双击运行时 Windows 会弹出 UAC 确认。
- 修复过程可能会短暂断开网络。
- Winsock/TCP/IP 重置后，通常需要重启电脑才能完全生效。
- 本工具不会删除个人文件，也不会修改安全软件设置。
