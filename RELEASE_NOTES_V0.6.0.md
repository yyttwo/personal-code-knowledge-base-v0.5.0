# PCKB 0.6.0 Public Preview

PCKB 现在支持 macOS Apple Silicon 和 Windows 11 x64。两个平台使用同一套产品界面和核心工作流，提供简体中文、English 与跟随系统三种语言选择。

PCKB 是 Local-first 的个人代码知识库：整理写过、学过和收藏过的代码，支持资产、Project、标签、学习记录、全文与结构化搜索、可选的语义搜索、关联代码、AI 辅助与 AI 对话，以及本地备份、恢复和废纸篓。AI 是可选增强功能，可选择本机 Ollama 或自行配置 DeepSeek、Qwen。

本版新增 Windows 原生 NSIS 安装器，并将 Windows 上的 API Key 保存到 Windows Credential Manager；macOS 继续使用钥匙串。Windows 文件系统、原子替换、备份/恢复与持久化流程已完成自动化验证。两平台的代码库仍由用户保存在自己选择的本地文件夹。

## 下载

- macOS Apple Silicon：[PCKB-0.6.0-Public-Preview-macOS-arm64.zip](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-macOS-arm64.zip) · [安装说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/INSTALL_MACOS.md)
- Windows 11 x64：[PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe) · [安装说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/INSTALL_WINDOWS.md)

请用本 Release 的 `SHA256SUMS.txt` 核对下载文件。

## 已知限制

- 本版是 Public Preview，不是稳定版；不提供自动更新或云同步。产品核心源代码目前仍为私有。
- macOS 仅支持 Apple Silicon，采用 ad hoc 签名；没有 Apple Developer ID 签名或 Apple 公证。
- Windows 仅支持 Windows 11 x64，安装器未进行 Authenticode 代码签名，SmartScreen 可能提示未知发布者。若缺少 Microsoft Edge WebView2 Runtime，安装过程可能需要联网下载。
- Ollama 模型需要用户自行安装，模型可用性与性能取决于本机硬件。DeepSeek、Qwen 是用户主动配置的可选云端服务。

## English summary

PCKB 0.6.0 Public Preview brings the same local-first personal code knowledge base to Apple Silicon macOS and Windows 11 x64, with Simplified Chinese, English, and System language selection. It includes a native Windows NSIS installer and uses Windows Credential Manager for cloud-provider API keys; macOS continues to use Keychain. Core library, search, learning, backup/restore, Trash, optional Ollama, DeepSeek, and Qwen workflows remain available.

This is a Public Preview with no automatic updates or cloud sync. The macOS build is ad hoc signed and not notarized; the Windows installer is unsigned and may trigger SmartScreen. WebView2 may require an internet download. Ollama models are user-managed and hardware-dependent. Core product source is currently private. Verify both downloads against `SHA256SUMS.txt`.
