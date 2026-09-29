# PCKB 0.6.0 Public Preview：Windows 安装说明

## 系统要求

- Windows 11 x64（AMD64）
- Microsoft Edge WebView2 Runtime；如果系统缺少所需组件，安装过程可能需要联网下载

当前不承诺 Windows 10 或 Windows ARM64 支持。Ollama 是可选功能，模型需要用户自行安装；本机运行性能取决于电脑硬件。

## 下载与校验

1. 从 [官方 v0.6.0 GitHub Release](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0) 下载 `PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe` 和 `SHA256SUMS.txt`。
2. 在下载目录打开 PowerShell，计算安装器 SHA-256：

   ```powershell
   Get-FileHash ".\PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe" -Algorithm SHA256
   ```

3. 确认结果与 `SHA256SUMS.txt` 中对应文件的值完全一致；不一致就不要运行。

## 安装

双击 NSIS 安装器，按提示完成安装。当前 Public Preview **未进行 Windows Authenticode 代码签名**。Windows Defender SmartScreen 可能显示“未知发布者”“Windows 已保护你的电脑”等提示。只有在确认下载来自上述官方 Release、且 SHA-256 匹配后，才考虑使用系统正常界面中的“更多信息”→“仍要运行”（More info → Run anyway）。不要关闭 Defender、SmartScreen 或 Windows Security，也不要修改注册表绕过保护。

打开 PCKB 后，可创建或打开本地代码库。代码库是用户数据，建议放在“文档”（Documents）或其他自己容易管理和备份的位置；不要放在 Program Files、Windows、System32 或安装器安装目录。卸载 PCKB 不会自动删除外部代码库。

PCKB 不提供自动更新。升级时，请从 GitHub Release 下载新版本并再次核对 SHA-256。DeepSeek / Qwen API Key 保存在 Windows Credential Manager，不写入代码库或备份；云端 AI 功能仅在用户配置并主动请求时使用。

## English summary

PCKB 0.6.0 Public Preview supports Windows 11 x64. Download the NSIS installer and `SHA256SUMS.txt` from the official release and verify the installer hash before running it. The installer is unsigned, so SmartScreen may show an unknown-publisher warning. WebView2 may need an internet download if its runtime is missing. Keep your library in a user-managed folder such as Documents; uninstalling PCKB does not delete an external library. There are no automatic updates.
