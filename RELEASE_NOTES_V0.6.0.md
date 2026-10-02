# PCKB 0.6.0 Public Preview

PCKB 现在支持 macOS Apple Silicon 和 Windows 11 x64。两个平台使用同一套产品界面和核心工作流，提供简体中文、English 与跟随系统三种语言选择。

PCKB 是 Local-first 的个人代码知识库：整理写过、学过和收藏过的代码，支持资产、Project、标签、学习记录、全文与结构化搜索、可选的语义搜索、关联代码、AI 辅助与 AI 对话，以及本地备份、恢复和废纸篓。AI 是可选增强功能，可选择本机 Ollama 或自行配置 DeepSeek、Qwen。

本版新增 Windows 原生 NSIS 安装器，并将 Windows 上的 API Key 保存到 Windows Credential Manager；macOS 继续使用钥匙串。Windows 文件系统、原子替换、备份/恢复与持久化流程已完成自动化验证。两平台的代码库仍由用户保存在自己选择的本地文件夹。

## 下载

- macOS Apple Silicon：[PCKB-0.6.0-Public-Preview-macOS-arm64.zip](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-macOS-arm64.zip) · [安装说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/INSTALL_MACOS.md)
- Windows 11 x64：[PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe) · [安装说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/INSTALL_WINDOWS.md)

请用本 Release 的 [SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/SHA256SUMS.txt) 核对下载文件。

## macOS — Apple Silicon

支持 Apple Silicon arm64（macOS 11.0+），当前不支持 Intel Mac。

1. 下载上方 `PCKB-0.6.0-Public-Preview-macOS-arm64.zip` 和校验文件。
2. 在下载目录的终端执行：

   ```sh
   shasum -a 256 PCKB-0.6.0-Public-Preview-macOS-arm64.zip
   ```

   预期 SHA256：`6827b45e9a2bdf87f9af2a56eec02b4fa2254277d5d357c654b73f5006e1a455`。只有与校验文件匹配才继续。
3. 双击 ZIP 解压得到 `PCKB.app`，将其拖入 Applications / 应用程序，再打开。
4. 本包使用 ad hoc 签名，没有 Apple Developer ID 签名或 Apple 公证。只有确认官方来源、哈希一致且你信任此来源后，若首次启动被拦截，使用 Finder → Applications → PCKB → Control-click / 右键 → Open / 打开 → 再确认打开（若系统提供）；或尝试打开后在系统设置 → 隐私与安全性 → 仍要打开 → 打开。不要关闭 Gatekeeper 或系统安全保护。若提示恶意软件或文件损坏，请停止并反馈。参见 [Apple 安全打开 App 说明](https://support.apple.com/102445)。
5. 更新时先退出旧 PCKB，下载、校验新版，再替换 Applications 中的旧 App；不要删除外部 Library。

## Windows 11 x64

本 Public Preview 的正式 Windows 支持范围为 Windows 11 x64，不承诺 Windows 10 或 ARM64。

1. 下载上方 `PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe` 和校验文件。
2. 在下载目录的 PowerShell 执行：

   ```powershell
   Get-FileHash ".\PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe" -Algorithm SHA256
   ```

   预期 SHA256：`27fce8290fd42bfd9a6ec7bdf37b44179012e9a505469522ccfc1c6ca76b7a55`。确认与 `SHA256SUMS.txt` 一致；大小写不影响比较。
3. 当前安装程序没有正式 Authenticode 签名，SmartScreen 可能提示 Windows protected your PC / Windows 已保护你的电脑。只有确认官方下载来源与 SHA256 完全匹配后，才使用 More info → Run anyway / 更多信息 → 仍要运行。不要关闭 Defender、SmartScreen 或实时保护，也不要修改注册表绕过安全功能。
4. 如果显示 Already Installed，推荐选择 Uninstall before installing；旧版卸载器中不要勾选 Delete the application data。
5. 保持安装器默认目录，不要自行改到 Program Files。若 Microsoft Edge WebView2 Runtime 尚未安装，安装器可能需要联网获取所需 Runtime。
6. 完成页可以保留 Run PCKB，Create desktop shortcut 按需选择，然后点击 Finish。
7. 创建或打开自己选择的外部 Library。它与程序安装目录分离，正常更新/卸载不应删除该 Library；请对重要代码资产保持正常备份。
8. Windows 的 API Key / Provider 凭据使用 Windows Credential Manager；macOS 使用 Keychain，不需要把 Key 写入明文配置文件。

## 隐私、更新与预览版说明

PCKB 是 local-first，Library 保存在你控制的位置。可选 AI 功能可能向你主动配置的 Provider 发送完成请求所需的内容，不会自动回退到其他云端 Provider。详见 [隐私说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/PRIVACY.md)。

PCKB Public Preview 当前不包含自动更新。新版本请从官方 GitHub Releases 页面重新下载安装。

PCKB 0.6.0 为 Public Preview（公开预览版）。核心工作流程已经在支持的平台上完成测试，但产品仍在持续开发中。

PCKB 应用源码保持私有；本公开仓库提供下载、文档、截图和版本信息。GitHub 自动生成的 Source code archive 不是 PCKB 应用源码。下载、安装和使用受 [EULA](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/legal/PCKB-EULA.txt) 约束，安装包包含第三方声明与许可证。

## 已知限制

- 本版是 Public Preview，不是稳定版；不提供自动更新或云同步。产品核心源代码目前仍为私有。
- macOS 仅支持 Apple Silicon，采用 ad hoc 签名；没有 Apple Developer ID 签名或 Apple 公证。
- Windows 仅支持 Windows 11 x64，安装器未进行 Authenticode 代码签名，SmartScreen 可能提示未知发布者。若缺少 Microsoft Edge WebView2 Runtime，安装过程可能需要联网下载。
- Ollama 模型需要用户自行安装，模型可用性与性能取决于本机硬件。DeepSeek、Qwen 是用户主动配置的可选云端服务。

## English summary

PCKB 0.6.0 Public Preview brings the same local-first personal code knowledge base to Apple Silicon macOS and Windows 11 x64, with Simplified Chinese, English, and System language selection. It includes a native Windows NSIS installer and uses Windows Credential Manager for cloud-provider API keys; macOS continues to use Keychain. Core library, search, learning, backup/restore, Trash, optional Ollama, DeepSeek, and Qwen workflows remain available.

This is a Public Preview with no automatic updates or cloud sync. The macOS build is ad hoc signed and not notarized; the Windows installer is unsigned and may trigger SmartScreen. WebView2 may require an internet download. Ollama models are user-managed and hardware-dependent. Core product source is currently private. Verify both downloads against `SHA256SUMS.txt`.
