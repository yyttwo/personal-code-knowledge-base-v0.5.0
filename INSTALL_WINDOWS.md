# PCKB 0.6.0 Public Preview：Windows 安装说明

## 系统要求

- Windows 11 x64（AMD64）
- Microsoft Edge WebView2 Runtime；如果系统缺少所需组件，安装过程可能需要联网下载

当前不承诺 Windows 10 或 Windows ARM64 支持。Ollama 是可选功能，模型需要用户自行安装；本机运行性能取决于电脑硬件。

不确定电脑类型时，可打开 Windows“设置”→“系统”→“关于”，查看 Windows 版本和“系统类型”。本下载适用于 Windows 11、基于 x64 的处理器。

## 下载与校验

1. 从 [官方 v0.6.0 GitHub Release](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0) 下载 `PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe` 和 `SHA256SUMS.txt`。
2. 在 Release 页面向下找到 **Assets**（发布附件），选择上面的 Windows `.exe` 文件。macOS `.zip` 是 Mac 版；GitHub 自动显示的 **Source code (zip / tar.gz)** 也不是 Windows 安装包。建议将两个文件保存在“下载”文件夹。
3. 在下载目录打开 PowerShell，计算安装器 SHA-256：

   ```powershell
   Get-FileHash ".\PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe" -Algorithm SHA256
   ```

4. 用记事本打开 `SHA256SUMS.txt`，找到 Windows 安装器对应的那一行。确认 PowerShell 输出的 Hash 与它完全一致（字母大小写不影响）；不一致就停止安装，重新从官方 Release 下载。

请始终使用同一 Release 的安装包和校验文件，不要混用旧 RC 或历史版本的 SHA。

## 安装

双击 NSIS 安装器，按提示完成安装。当前 Public Preview **未进行 Windows Authenticode 代码签名**。Windows Defender SmartScreen 可能显示“未知发布者”“Windows 已保护你的电脑”等提示。只有在确认下载来自上述官方 Release、且 SHA-256 匹配后，才考虑使用系统正常界面中的“更多信息”→“仍要运行”（More info → Run anyway）。不要关闭 Defender、SmartScreen 或 Windows Security，也不要修改注册表绕过保护。

安装器使用 Microsoft Edge WebView2 显示界面。如果系统缺少所需 Runtime，安装过程可能联网获取组件；请等待安装完成。完成后从开始菜单打开 **PCKB**。

## 第一次使用

1. 在欢迎页选择“创建新的代码库”，并选择一个新的空文件夹；已有 PCKB 代码库则选择“打开已有代码库”。
2. 代码库是用户自己的数据。建议放在“文档”（Documents）或其他自己容易管理和备份的位置；不要放在 Program Files、Windows、System32 或安装器安装目录。
3. 用“新建资产”保存代码、用途和笔记，或通过“导入代码文件”导入单个文件。随后可以按 Project、标签、常用和学习状态整理，并用搜索找到代码。
4. 在设置中选择简体中文、English 或跟随系统。AI 功能是可选项，不配置 AI 也能使用本地代码库、普通搜索、学习、备份和废纸篓。

DeepSeek / Qwen API Key 保存在 Windows Credential Manager，不写入代码库或备份；云端 AI 功能仅在用户配置并主动请求时使用。Ollama 需要用户自行安装兼容环境与模型。

## 升级与卸载

PCKB 不提供自动更新。升级前建议在旧版本中创建有效备份，退出 PCKB，再从官方 GitHub Release 下载新安装器并核对 SHA-256。安装新版后打开原来的代码库，检查资产、Project 和学习记录；如设置提示语义索引需要重建，再按提示操作。

卸载可通过 Windows“设置”→“应用”→“安装的应用”中 PCKB 的正常卸载入口进行。卸载 PCKB 不会自动删除外部代码库。保留代码库和备份即可继续管理自己的数据；系统凭据也不一定随卸载删除，如需移除 API Key，可先在 PCKB 设置中删除，或使用 Windows“凭据管理器”管理相应项目。

## English summary

PCKB 0.6.0 Public Preview supports Windows 11 x64. Download the NSIS installer and `SHA256SUMS.txt` from the official release and verify the installer hash before running it. The installer is unsigned, so SmartScreen may show an unknown-publisher warning. WebView2 may need an internet download if its runtime is missing. Keep your library in a user-managed folder such as Documents; uninstalling PCKB does not delete an external library. There are no automatic updates.
