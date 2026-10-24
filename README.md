# Quiet RDP · Tails 下载

适用于 **Tails 7 / amd64（64 位 Intel、AMD 电脑）**。只下载下面这一个文件。

## [下载 Quiet RDP 0.3.1](https://github.com/tom062119/quiet-rdp-download/releases/latest/download/Quiet-RDP-Tails-amd64.run)

[打开最新版发布页](https://github.com/tom062119/quiet-rdp-download/releases/latest)

### 如何使用

1. 用 Tails 浏览器下载 `Quiet-RDP-Tails-amd64.run`。
2. 在文件管理器中右键该文件 → **属性 → 权限 → 允许作为程序执行**。这是首次下载文件的执行许可。
3. **双击打开**。会显示安装进度，加入应用菜单，并自动打开 Quiet RDP。
4. 等 Tor 连接完成，登录管理员分配的账号，再双击服务器名称连接。

不需要输入命令，不需要管理员密码，不需要另装 Remmina、torsocks 或 RDP 插件。若文件所在位置不允许执行，可用文件管理器将它移动到个人文件夹后再打开。

程序只安装到本次开机的内存目录。**不写入 Persistent，不提供持久化安装；每次重启 Tails 后重新下载。** 登录、授权同步和 RDP 连接需要网络；安装过程不联网。账号由管理员创建，不开放注册。

### 0.3.1 当前试用包

- 远程桌面独立窗口、默认最大化、按钮切换全屏、双向剪贴板、动态分辨率。
- 自动画质、极省流选项和网络中断后自动重连。
- 管理员分配服务器；Tor 公网或管理员授权的 Onion 线路。
- 补充 Windows 自动登录请求，处理首次认证后停留在登录界面的问题。具体目标 Windows 尚需实际确认。
- 人工确认的证书指纹只在本次软件运行内复用，退出软件即清除。

**本次只完成编译与文件完整性核对，没有执行完整功能测试、真实 Tails 安装或目标 Windows 连接验收。** 本页保留一个当前版本，不提供多个客户端变体。安装器不是 AppImage，也不需要 FUSE。

### 许可与完整性

Quiet RDP 自有代码使用 [二进制分发许可](LICENSE)，客户端源码不在本仓库公开。安装文件中的 `LICENSE`、`THIRD-PARTY-NOTICES.txt` 和 `licenses/` 保留相应声明。

本软件使用 [FFmpeg](https://ffmpeg.org/) 的 LGPL-2.1-or-later 动态库，以及 FreeRDP、GTK/GLib 等组件。[第三方对应源码及构建说明](https://github.com/tom062119/quiet-rdp-download/releases/download/v0.3.1/quiet-rdp-0.3.1-third-party-sources.tar.gz)仅用于满足这些库的分发许可，**正常安装不需要下载**。它不包含 Quiet RDP 的业务源码。

可在发布页查看 `SHA256SUMS`。程序已去除调试符号；校验用于发现文件损坏，不是“不可逆向”的承诺。本项目尚未加入 Tails/Debian 官方 APT 仓库。
