# Quiet RDP · Tails 下载

适用于 **Tails 7 / amd64（64 位 Intel、AMD 电脑）**。正常使用只下载这一个文件。

## [下载 Quiet RDP 0.4.0](https://github.com/tom062119/quiet-rdp-download/releases/latest/download/Quiet-RDP-Tails-amd64.run)

[打开最新版发布页](https://github.com/tom062119/quiet-rdp-download/releases/latest)

### 如何使用

1. 用 Tails 浏览器下载 `Quiet-RDP-Tails-amd64.run`。更新前先退出旧版 Quiet RDP。
2. 在文件管理器中右键该文件 → **属性 → 权限 → 允许作为程序执行**。
3. **双击打开**。安装器显示进度、加入应用菜单并自动打开软件。
4. 等 Tor 连接完成，登录管理员分配的账号，再双击服务器名称连接。

不需要输入命令或管理员密码，不需要另装 Remmina、torsocks 或 RDP 插件。若下载位置禁止执行，可用文件管理器将文件移到个人文件夹后打开。

程序只安装到本次开机的内存目录。**不提供持久化安装；重启 Tails 后重新下载。** 安装过程不联网；登录、同步和远程连接需要网络。账号由管理员创建，不开放注册。

### 0.4.0 新增

- **五笔输入**：登录后打开“工具”，按需启用极点五笔 86 或海峰五笔 86。首次启用后在 Tails 右上角输入法菜单中选择；远程输入中文时选择客户端的“Tails 输入法”。
- **截图标注**：在“工具”中启用 Alt+A，使用 GNOME 截图选区，然后标注、复制或保存。复制的图片可通过双向剪贴板粘贴到远程桌面。
- **快捷网址**：管理员在后台配置入口并分配用户；客户端自动同步并显示按钮，通过 Tor 浏览器打开。
- **Telegram**：在“工具”中点击下载并打开，经 Tor 下载固定的官方 7.3.3 版本并校验 SHA-256，运行文件和会话放在内存目录。首次启动仍需确认 Telegram 的代理提示。

保留远程桌面独立窗口、默认最大化、按钮切换全屏、双向剪贴板、动态分辨率和网络中断后自动重连。服务器由管理员分配；Tor 公网与管理员授权的 Onion 线路均可用。新增工具不会自动开启。

**本次完成编译、打包和文件完整性核对；没有执行完整功能测试、真实 Tails 安装或 Windows 连接验收。** 五笔菜单、截图窗口和 Telegram 代理仍需在你的 Tails 上实测。安装器不是 AppImage，不需要 FUSE。

### 许可与完整性

Quiet RDP 自有代码使用 [二进制分发许可](LICENSE)。本仓库不发布客户端源码包、后端代码、账号数据或密钥。安装器包含运行所需的桌面助手、第三方组件及各自许可。

[第三方对应源码及构建说明](https://github.com/tom062119/quiet-rdp-download/releases/download/v0.4.0/quiet-rdp-0.4.0-third-party-sources.tar.gz)用于提供 FreeRDP、FFmpeg、GTK/GLib 和五笔输入法等组件的对应源码；**正常安装不需要下载**。它不是另一个客户端版本，也不包含 Quiet RDP 的业务源码。第三方许可证不受自有代码许可变更影响。

发布页的 `SHA256SUMS` 用于核对文件完整性。程序已去除调试符号，不能据此承诺无法逆向分析。本项目与 Tails 官方没有隶属关系，尚未加入 Tails/Debian 官方 APT 仓库。
