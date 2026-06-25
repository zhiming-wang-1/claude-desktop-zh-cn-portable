# Claude Desktop zh-CN Portable

Windows Claude Desktop 中文绿色版生成工具。

本项目用于从你本机已安装的 Claude Desktop，或官方来源下载的 MSIX，生成一个独立的中文绿色版副本。它默认生成在 `%LOCALAPPDATA%\ClaudeZhCN`，使用独立用户数据目录 `%APPDATA%\ClaudeZhCN-3p`，尽量避免修改和影响官方 Claude Desktop。

> 本项目不是 Anthropic 官方项目，不分发 Claude Desktop 官方程序、安装包、账号数据、API key 或访问令牌。使用前请阅读 [DISCLAIMER.md](DISCLAIMER.md)。

## 适合谁

- 想在 Windows 上使用中文界面的 Claude Desktop。
- 不想直接修改官方 Claude Desktop 安装目录。
- 希望官方版和中文绿色版可以共存。
- 不熟悉命令行，希望双击工具完成安装、更新、修复。

## 不适合谁

- 想下载一个已经打包好的 Claude 完整程序。
- 想绕过 Claude 官方登录、订阅或地区限制。
- 想修改官方 Microsoft Store/Appx 安装目录。

## 快速开始

1. 下载本仓库 Release 包并解压。
2. 双击运行：

```text
cc_desktop_tool.bat
```

也可以双击中文入口：

```text
cc_desktop_tool_zh.bat
```

3. 第一次使用选择：

```text
1. First install / initialize
```

4. 安装完成后，从桌面或开始菜单启动：

```text
Claude zh-CN
```

请尽量使用 `Claude zh-CN` 快捷方式启动，不要直接双击绿色版目录里的 `Claude.exe`，否则可能绕过独立用户数据和登录回调修复逻辑。

## 生成位置

默认路径如下：

```text
绿色版程序：%LOCALAPPDATA%\ClaudeZhCN\Claude
绿色版启动器：%LOCALAPPDATA%\ClaudeZhCN\launch_claude_zh_cn.vbs
绿色版用户数据：%APPDATA%\ClaudeZhCN-3p
桌面/开始菜单入口：Claude zh-CN
```


## 常用菜单

```text
1  First install / initialize
2  Launch zh-CN Claude
3  Check for updates
4  Update / rebuild zh-CN portable Claude
8  Show paths / diagnostics
9  Shortcut manager
11 Clean / reset / uninstall
12 Dual launch / OAuth login repair
0  Exit
```

如果网页登录成功后自动打开官方版，而绿色版仍停在登录页，请使用菜单 `12 Dual launch / OAuth login repair` 修复登录回调。


## 与直接汉化官方版的区别

直接汉化官方 Claude Desktop 通常会修改官方安装目录中的资源文件，例如 `app.asar`。这在 Microsoft Store/Appx 版上风险更高，可能导致更新失败、重启后打不开、签名校验异常，或 Claude Code/Cowork 等功能异常。

本项目采用绿色版副本思路：复制官方来源的本地应用到独立目录，再对副本做中文本地化。这样更适合普通用户长期使用。

## 修复官方版

如果你曾经直接修改过官方 Claude Desktop，导致官方版打不开，建议：

1. 打开 Windows 设置。
2. 进入“应用”。
3. 找到 Claude。
4. 选择“高级选项”。
5. 先尝试“修复”。
6. 如果仍失败，卸载后从 Microsoft Store 重新安装。

修复官方版后，建议保持官方版原样，中文界面使用绿色版。


## 来源与许可

本项目基于社区绿色版方案整理，保留 MIT License。详见 [LICENSE](LICENSE) 和 [NOTICE.md](NOTICE.md)。

Claude、Claude Desktop、Claude Code、Anthropic 等名称属于其各自权利人。本项目仅为独立社区工具。
