# 如何在 Vultr 云服务器上重置 Root 密码

## 前言
当您因忘记密码而无法访问 root 账户时，可以通过单用户模式进行密码重置。本指南将详细介绍如何通过 Web 控制台连接服务器，进入单用户模式，并完成 root 密码的重置操作。

## 准备工作
在开始操作系统特定步骤前，请先完成以下基础操作：

1. 在 [Vultr 客户门户](https://bit.ly/VuLtr) 点击 **Server Restart** 图标
2. 打开 Web 控制台
3. 根据您的操作系统选择对应的重置方案

👉 [【点击查看】2025年最新 Vultr 优惠码及特价云服务器方案汇总](https://bit.ly/VuLtr)

## 各操作系统重置指南

### AlmaLinux
1. 系统启动时按 Esc 调出 GRUB 引导菜单
2. 按 E 编辑第一个启动项
3. 找到以 `linux` 开头的内核行
4. 将 `ro` 改为 `rw init=/sysroot/bin/sh`
5. 按 Ctrl+X 或 F10 进入单用户模式
6. 执行 `chroot /sysroot` 访问系统
7. 使用 `passwd` 命令修改密码
8. 运行 `touch /.autorelabel` 强制文件系统重新标记（SELinux 系统必需）
9. 依次执行 `exit`、`logout` 和 `reboot`

### Arch Linux
1. 启动时按 Esc 进入 GRUB 菜单
2. 按 E 编辑启动项
3. 在 `linux /boot/` 行末添加 `init=/bin/bash`
4. 按 Ctrl+X 启动
5. 执行 `mount -o remount,rw /` 挂载系统
6. 使用 `passwd` 修改密码
7. 通过 `exec /sbin/init` 重启

### CentOS 系列
各版本 CentOS 操作类似，主要区别在于：
- CentOS 6：在 GRUB 提示符后追加 `single`
- CentOS 7/8/9：修改内核参数为 `rw init=/sysroot/bin/sh`
- 均需执行 SELinux 重新标记操作

### CoreOS
1. 编辑 GRUB 启动项时添加 `coreos.autologin=tty1`
2. 以 core 用户身份登录后执行 `sudo passwd`
3. 建议完成密码重置后锁定 core 用户密码

### Debian/Ubuntu
1. GRUB 编辑时在 `linux /boot/` 行添加 `init=/bin/bash`
2. 需要手动重新挂载系统为可写状态
3. 密码修改后通过 `exec /sbin/init` 重启

### FreeBSD
1. 启动菜单选择 2 进入单用户模式
2. 执行 `mount -u -a -o rw` 重新挂载
3. 直接使用 `passwd` 修改密码

### Windows Server
需使用 SystemRescue ISO 进行救援：
1. 创建系统备份（必需步骤）
2. 挂载救援 ISO 并启动
3. 使用 `chntpw` 工具清除管理员密码
4. 移除 ISO 后通过控制台设置新密码

## 注意事项
- 所有操作都需要在 Web 控制台中完成
- SELinux 系统必须执行 `/.autorelabel` 操作
- Windows 系统重置后必须通过控制台设置新密码
- 建议定期备份重要数据

👉 [立即获取 Vultr 高性能云服务器专属优惠](https://bit.ly/VuLtr)