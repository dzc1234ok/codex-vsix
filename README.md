# Codex VSIX

通过 GitHub Actions 从 Microsoft Visual Studio Marketplace 获取 OpenAI 官方 Codex VS Code 扩展（`openai.chatgpt`）的最新稳定版 Windows x64 VSIX，并发布到 GitHub Releases。

## 下载

前往 [Releases](https://github.com/dzc1234ok/codex-vsix/releases/latest) 下载：

- `openai.chatgpt-<版本号>-win32-x64.vsix`
- 同名的 `.sha256` 校验文件

当前已发布版本：`26.908.40401`。

## 安装

在 PowerShell 中执行：

```powershell
code --install-extension .\openai.chatgpt-26.908.40401-win32-x64.vsix
```

也可以在 VS Code 中按 `Ctrl+Shift+P`，选择 **Extensions: Install from VSIX...**。

## 获取后续新版本

进入仓库的 **Actions → Build latest Codex VSIX → Run workflow**。工作流会自动：

1. 查询 Marketplace 的最新稳定版 Windows x64 包；
2. 从 Marketplace CDN 下载官方 VSIX；
3. 校验扩展 ID、版本、ZIP 完整性和 Marketplace SHA-256；
4. 上传 Actions Artifact；
5. 创建或更新对应的 GitHub Release。
