# PCKB 0.7.0 Public Preview

**本次更新仅支持 macOS Apple Silicon（arm64），暂不提供 Windows 新版本。**

## 主要更新

- 新增 AI Workbench V1。
- **Ask：** AI 询问与对话。
- **Code：** 找问题、讲解代码、修改预览、明确应用与撤销，以及复制代码。
- **Project：** 需求分析、项目方案、文件生成、检查，以及整个项目的文件夹 / 源码 ZIP 导出。
- **Learning：** 分级提示、代码讲解、参考答案与学生代码点评。
- **PCKB Knowledge：** 主动选择已有代码资产作为 AI 上下文，并查看回答的参考来源。
- **Save to PCKB：** 从工作台预览后新建代码资产，检测相同代码并避免重复保存。更新已有资产仍通过“全部资产 → 编辑”完成。
- 改进工作台会话废纸篓的可发现性与恢复体验。
- 优化保存代码时的语言自动识别。
- 修复 Markdown 表格显示和代码点评文件名一致性问题。

## 下载与安装

- [PCKB-0.7.0-Public-Preview-macOS-arm64.zip](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.0/PCKB-0.7.0-Public-Preview-macOS-arm64.zip)
- [SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.0/SHA256SUMS.txt)
- [macOS 安装说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/INSTALL_MACOS.md)

系统要求：Apple Silicon arm64，macOS 11.0 或更高版本。不支持 Intel Mac。

1. 下载 ZIP 与同一 Release 的 `SHA256SUMS.txt`。
2. 用 `shasum -a 256 PCKB-0.7.0-Public-Preview-macOS-arm64.zip` 核对校验值；不一致时停止安装。
3. 解压得到 `PCKB.app`，拖入 Applications / 应用程序。
4. 更新前退出旧 App；保留外部 Library、工作台应用数据与正常备份。

本包使用 **ad hoc 签名，没有 Apple Developer ID 签名，也没有 Apple 公证**。若 macOS 阻止首次启动，仅在官方来源及校验值确认后，通过 Finder 的正常 Open / 打开或系统设置 → 隐私与安全性 → 仍要打开流程处理。不要关闭 Gatekeeper 或系统安全保护；若提示恶意软件或文件损坏，请停止并反馈。

## 使用与隐私说明

- 本版本仍为 Public Preview，不是稳定版；不提供自动更新或云同步。
- 新版 AI Workbench 云端功能需要自行配置受支持的 DeepSeek 或 Qwen Provider / 模型与 API Key。凭据由可信后端通过 macOS 钥匙串处理，不回填到输入框。
- 既有资产 AI 辅助与 Embedding 配置仍与工作台设置区分；不会自动切换到其他云端 Provider。
- 云端请求会发送完成用户所选任务所需的问题及明确选择的代码 / 上下文。请勿提交真实凭据或不适合交给第三方的代码，详见[隐私说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/PRIVACY.md)。
- PCKB **不会自动执行生成代码**，不会自动覆盖原始文件或外部开发项目。应用修改只改变工作台副本；复制或导出后请在自己的环境验证。
- OpenCodeReview 智能项目深度审查不属于本次发布内容。

## Windows 历史版本

本次没有 Windows v0.7.0 安装包。Windows 用户可以继续下载[历史 v0.6.0 Release](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0)中的 [Windows 11 x64 安装程序](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe)，并使用其对应的 [v0.6.0 SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/SHA256SUMS.txt) 与 [Windows 安装说明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/INSTALL_WINDOWS.md)。

Windows v0.6.0 保留其原有功能，**不包含此次新增的全部 AI Workbench 功能**。旧 Release 与安装包继续保留用于使用及回退。

## 源码与许可

PCKB 核心源码保持私有。本公开仓库仅提供产品文档、已审核图片、法律与第三方许可材料以及二进制发行信息。GitHub 自动生成的 Source code archives 只包含公开文档仓库，不是 PCKB 应用源码。

下载、安装和使用受 [PCKB EULA](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/legal/PCKB-EULA.txt) 约束；第三方开源组件继续适用各自许可证。请同时阅读[第三方声明](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/legal/THIRD-PARTY-NOTICES.txt)、[组件源码出处](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/blob/main/legal/OPEN-SOURCE-COMPONENT-SOURCES.md)与[开源许可证文本](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/tree/main/legal/OPEN-SOURCE-LICENSES)。

## English platform and installation summary

PCKB 0.7.0 Public Preview is **macOS Apple Silicon Only**: arm64 on macOS 11.0 or later. There is no new Windows installer. Historical Windows v0.6.0 remains available, but it does not include all of the new AI Workbench features.

This Mac release adds AI Workbench V1 with Ask, Code analysis/explanation/change previews/apply/undo, Project planning and folder/source ZIP export, Learning help, explicitly selected PCKB Knowledge context, and new-asset saving with duplicate detection. It also improves recoverable Session Trash, language detection, Markdown tables, and code-review filenames. Update existing library assets through All Assets → Edit; the Workbench does not provide an overwrite shortcut.

Download the Mac ZIP and matching `SHA256SUMS.txt`, verify the checksum, extract `PCKB.app`, and drag it into Applications. Quit the old App before replacing it; retain your external Library and normal backups. The App is ad hoc signed, **not Apple Developer ID signed or notarized**. Use the normal macOS graphical Open / Open Anyway flow after verifying the official source and checksum; do not disable system protection.

Cloud Workbench features require your own supported DeepSeek or Qwen API key, stored through macOS Keychain. PCKB does not execute generated code or automatically overwrite external projects. OpenCodeReview is not part of this release. This remains a Public Preview with no automatic updates; core application source is private, and GitHub's automatic Source code archives contain only the public documentation repository.
