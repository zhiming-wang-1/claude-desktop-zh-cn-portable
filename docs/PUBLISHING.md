# Publishing

这个仓库可以公开发布，但请只发布源码、脚本、词库和文档。

## GitHub 创建仓库

推荐仓库名：

```text
claude-desktop-zh-cn-portable
```

推荐描述：

```text
Windows Claude Desktop 中文绿色版生成工具，不分发 Claude 官方程序。
```

推荐 topics：

```text
claude
claude-desktop
windows
zh-cn
localization
portable
electron
```

## 发布前检查

确认仓库里没有：

```text
Claude.exe
app.asar
icudtl.dat
*.msix
*.appx
*.msixbundle
*.appxbundle
ClaudeZhCN
ClaudeZhCN-3p
Cookie
token
API key
```

可以用下面命令粗略检查：

```powershell
git status --short
git ls-files
```

## Release 建议

Release 包只打包仓库源码，不要包含生成后的 Claude 绿色版程序。

可以发布这样的说明：

```text
本 Release 仅包含绿色版生成工具、中文词库和文档。
不包含 Claude Desktop 官方程序、安装包、账号数据或访问令牌。
```
