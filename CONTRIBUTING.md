# Contributing

欢迎贡献中文词条、界面截图对应的漏翻修复、Windows 兼容性修复和文档改进。

## 提交前检查

请确认你的提交没有包含：

```text
Claude 官方程序
官方安装包
app.asar
Claude.exe
icudtl.dat
账号数据
Cookie
token
API key
绿色版生成目录
```

## 推荐贡献方式

1. 先创建一个新分支。
2. 修改脚本、词库或文档。
3. 本地运行一次基础检查。
4. 提交 Pull Request，并说明你修复了哪个页面或哪个问题。

## 本地检查

如果你安装了 Python，可以运行：

```powershell
python -m py_compile .\cc_desktop_zh_cn_windows.py
```

如果只是改文档或词条，也请确认仓库中没有误加入官方 Claude 文件。
