# PCKB

Personal Code Knowledge Base · 个人代码知识库

把你写过、学过和收藏过的代码，变成一个可以搜索、理解和直接提问的个人代码知识库。

管理、搜索、理解自己的代码资产。支持本地 AI、多模型和语义检索，让自己的代码真正成为可用的知识库。

[简体中文](README.md) | [English](README.en.md)

**PCKB 0.7.1 Public Preview · macOS Apple Silicon Only · 简体中文 + English**

**本次 v0.7.1 仅提供 macOS Apple Silicon（arm64）安装包，不提供 Windows 新版本。** Windows 用户仍可下载历史 v0.6.0；该版本不包含此次新增的全部 AI Workbench 功能。

## Download / 下载

**[PCKB 0.7.1 Public Preview — macOS Apple Silicon Only](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.7.1)**

| 平台 / Platform | 系统要求 / Requirements | 下载 / Download |
| --- | --- | --- |
| macOS · v0.7.1 | Apple Silicon arm64 · macOS 11.0+ | [macOS ZIP](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.1/PCKB-0.7.1-Public-Preview-macOS-arm64.zip) |
| Windows · 历史 v0.6.0 | Windows 11 x64 | [历史 Windows 安装程序](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe) |

安装新版 Mac 包前，请核对 [v0.7.1 SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.1/SHA256SUMS.txt)。历史 Windows 包必须使用 [v0.6.0 SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/SHA256SUMS.txt)。GitHub 自动提供的 Source code archive 仅是这个下载与文档仓库的归档，不是 PCKB 应用源码。

PCKB 适合保存自己写过的代码片段、项目中值得复用的实现，以及学习过程中收藏的示例。每条代码可以连同用途、笔记、标签、Project 和学习记录一起整理；以后既能按关键词查找，也能在配置向量模型后用语义搜索找回“记得意思、忘了名字”的代码。

你可以先把它当作纯本地代码知识库使用，再按需要开启 AI 讲解、改进建议或工作台。普通代码库管理、全文与结构化搜索、资产学习记录、备份和废纸篓不要求配置 AI。数据由用户保存在自己选择的位置；云端 AI 是用户主动选择的增强功能。v0.7.1 新增的 AI Workbench V1 本次仅在 Mac 版提供，不代表历史 Windows v0.6.0 具有相同的新功能。

### macOS — Apple Silicon

Apple Silicon / arm64，macOS 11.0 或更高版本：[PCKB-0.7.1-Public-Preview-macOS-arm64.zip](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.1/PCKB-0.7.1-Public-Preview-macOS-arm64.zip)。

使用 ad hoc 签名，**没有** Apple Developer ID 签名或 Apple 公证。安装说明：[INSTALL_MACOS.md](INSTALL_MACOS.md)。

下载 ZIP → 在终端运行 `shasum -a 256 PCKB-0.7.1-Public-Preview-macOS-arm64.zip` 并与校验文件比较 → 解压得到 `PCKB.app` → 拖入 Applications / 应用程序 → 打开。若首次启动被系统拦截，仅在官方来源与 SHA256 都确认后，使用 Finder 中 Control-click / 右键 → Open / 打开 → 再确认打开（若系统提供该选项），或系统设置 → 隐私与安全性 → 仍要打开。不要关闭系统安全保护。更新时先退出旧 App，再替换 App，保留外部 Library；完整步骤见安装说明。

### Windows 11 x64 — 历史 v0.6.0

Windows 11 / x64：[PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe)。

本次没有 Windows v0.7.1 安装包；下列 v0.6.0 下载与安装说明继续保留。历史 NSIS 安装器**没有** Windows 代码签名，SmartScreen 可能提示未知发布者。安装说明：[INSTALL_WINDOWS.md](INSTALL_WINDOWS.md)。请使用 v0.6.0 Release 内的 `SHA256SUMS.txt` 校验此 Windows 包。

下载 Setup.exe → 在 PowerShell 运行 `Get-FileHash ".\PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe" -Algorithm SHA256` → 确认结果为 `27fce8290fd42bfd9a6ec7bdf37b44179012e9a505469522ccfc1c6ca76b7a55` → 安装。仅在官方来源与哈希匹配后，才使用 SmartScreen 的“更多信息 → 仍要运行”；不要关闭 Defender 或 SmartScreen。若提示 Already Installed，选择 Uninstall before installing，且不要勾选 Delete the application data；保持安装器默认目录。完成页可保留 Run PCKB，桌面快捷方式按需选择，再点击 Finish。缺少 WebView2 Runtime 时安装器可能需要联网下载。外部 Library 与安装目录分离，请保留正常备份；完整步骤见安装说明。

![PCKB 代码库与代码详情](screenshots/public/01-main-library.png)

PCKB 仍在持续开发中。本仓库是公开二进制发布仓库，不包含产品核心源代码。

以下均为使用虚构演示代码库拍摄的真实 PCKB 截图。本机私人路径已用不透明色块遮挡，其他产品内容未修改。

这些已审核的截图来自此前 macOS 版本，展示已有资产库功能，不是新版 AI Workbench 的完整截图。历史 Windows v0.6.0 的原有核心资产库功能仍可使用；本次 Mac 的新增工作台功能不能据此视为 Windows 已支持。

## v0.7.1 修复

- 修复 AI 工作台会话 `⋯` 菜单重叠、残留及列表边缘裁切。
- 同时只显示一个菜单，切换菜单、点击外部、Esc、滚动或调整窗口时正确关闭。
- 重命名、会话废纸篓及恢复行为保持不变；没有新增 AI 功能或数据库格式变更。

## 功能

- 完整简体中文 / English 界面，可跟随系统或在 App 内即时切换
- 个人代码资产库、Project、标签、常用、学习状态和验证记录
- 全文搜索、结构化筛选、可选的语义/混合搜索和关联代码
- 安全的单文件导入、可恢复废纸篓和本地备份/恢复
- AI 代码辅助，以及 Mac v0.7.0 新增的 AI Workbench V1
- 仅保存在本机的自定义 App 背景

## AI Workbench V1 — Mac v0.7.0

- **Ask：** AI 询问与对话。
- **Code：** 找问题、讲解代码、生成修改预览；确认后应用到本地工作副本，也可撤销和复制代码。
- **Project：** 需求分析 → 项目方案 → 文件生成 → 检查 → 文件夹或源码 ZIP 导出。
- **Learning：** 分级提示、先讲解后给代码、参考答案和学生代码点评。
- **PCKB Knowledge：** 主动选择已有代码资产作为本次 AI 上下文，回答可以查看参考来源。
- **Save to PCKB：** 预览后新建代码资产，检测相同代码，避免重复保存。更新已有资产仍通过“全部资产 → 编辑”完成。
- 会话可移入工作台会话废纸篓并恢复；本版还优化代码语言自动识别、Markdown 表格和代码点评文件名显示。

工作台使用独立保存的 DeepSeek 或 Qwen Provider / 模型设置；云端功能需要用户自行配置受支持的 API Key。修改不会自动覆盖原始文件，PCKB **不会自动执行生成代码**。请复制或导出后在自己的开发环境检查与运行。

OpenCodeReview 智能项目深度审查不属于本次发布内容。

## 产品截图

### 收集与整理

| 新建代码资产 | 管理项目 |
| --- | --- |
| ![新建代码资产](screenshots/public/02-new-asset.png) | ![项目管理](screenshots/public/03-project-management.png) |

### 学习与复习

| 学习中心概览 | 资产学习卡片 |
| --- | --- |
| ![学习中心概览](screenshots/public/04-learning-overview.png) | ![资产学习卡片](screenshots/public/05-learning-assets.png) |

### 设置与保护

| AI 与智能搜索设置 | 备份与恢复 |
| --- | --- |
| ![AI 与智能搜索设置](screenshots/public/06-ai-settings.png) | ![本地备份与恢复](screenshots/public/07-backup-restore.png) |

### 自定义外观

![本机 App 背景设置](screenshots/public/08-app-background.png)

保留的截图仅展示既有资产库、设置和外观；新版工作台功能请参见上方介绍与[用户指南](USER_GUIDE.md)。

## AI 选项

- **Ollama：** 可选的本机生成与向量能力
- **DeepSeek API：** 可选的自备 Key 生成与 AI 对话
- **Qwen API：** 可选的自备 Key 生成、AI 对话与向量能力
- Generation 和 Embedding Provider 相互独立
- AI Workbench V1 使用单独的 DeepSeek / Qwen 设置，不会自动沿用或切换到其他 Provider
- API 凭据在 macOS 使用钥匙串，在 Windows 使用 Windows Credential Manager 保存
- 不会自动回退到其他云端 Provider

云端 AI 操作会把完成用户主动请求所需的内容发送给所选 Provider。完整边界见 [PRIVACY.md](PRIVACY.md)。

App 提供内置 PCKB 夜湖背景，也支持选择本地图片，调整遮罩、模糊与 Cover/Contain 显示方式。背景图片保存在本机。

## 快速开始

1. 新版 Mac 用户下载上方 v0.7.1 ZIP；Windows 用户下载历史 v0.6.0 安装器。分别核对对应 Release 的 SHA-256。
2. 按 [macOS 安装说明](INSTALL_MACOS.md) 或[历史 Windows 安装说明](INSTALL_WINDOWS.md)安装。
3. 打开 PCKB，创建或打开本地代码库。

Windows 用户可直接按[历史 v0.6.0 下载、安装与首次使用指引](INSTALL_WINDOWS.md)逐步操作。第一次使用时，可以先保存一条代码资产，为它补上用途和标签，再试试搜索、Project 分类与学习状态。Mac 用户需要新版工作台时，进入“设置 → AI 工作台”配置 Provider、模型与 API 凭据。

## 隐私

代码库主要以普通文件保存在用户选择的本机文件夹中。Ollama 支持本机 AI 工作流；DeepSeek 与 Qwen 是可选的外部 BYOK Provider。PCKB 不会自动切换到其他云端 Provider。

PCKB 应用源码当前保持私有。本公开仓库仅用于官方下载安装包、文档、截图与版本发布信息。

## Updates / 更新

PCKB Public Preview 当前不包含自动更新。新版本请从[官方 GitHub Releases 页面](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases)重新下载安装。

PCKB 0.7.1 为仅面向 macOS Apple Silicon 的 Public Preview（公开预览版）。产品仍在持续开发中；Windows 新版尚未发布。

## 文档

- [v0.7.1 Release Notes](RELEASE_NOTES_V0.7.1.md)
- [v0.7.0 Release Notes](RELEASE_NOTES_V0.7.0.md)
- [macOS 安装说明](INSTALL_MACOS.md)
- [Windows 安装说明](INSTALL_WINDOWS.md)
- [用户指南](USER_GUIDE.md)
- [隐私说明](PRIVACY.md)
- [安全反馈](SECURITY.md)
- [源代码状态](SOURCE_CODE_NOTICE.md)

## 法律说明

PCKB 以专有免费软件形式分发。下载、安装或使用 PCKB 均受 [PCKB EULA](legal/PCKB-EULA.txt) 约束。第三方开源组件继续适用各自许可证；请同时阅读[第三方声明](legal/THIRD-PARTY-NOTICES.txt)、[组件源码出处](legal/OPEN-SOURCE-COMPONENT-SOURCES.md)和[开源许可证文本](legal/OPEN-SOURCE-LICENSES/)。

## 已知限制

- macOS 仅支持 Apple Silicon（arm64），没有 Apple Developer ID 签名或 Apple 公证；当前不支持 Intel Mac。
- 本次不提供 Windows v0.7.1。历史 v0.6.0 仅支持 Windows 11 x64，安装器未做代码签名，SmartScreen 可能提示未知发布者；当前不承诺 Windows 10 或 ARM64。
- 不提供云同步、自动更新、文件夹批量导入、Git/GitHub 同步、VS Code 扩展或代码执行。
- Ollama 模型需要用户自行安装和管理；DeepSeek 与 Qwen 需要用户自己的 API Key、网络连接及服务额度。
- 当前是持续开发中的公开预览版，不是稳定版或功能完整版本。
- OpenCodeReview 智能项目深度审查不在本次版本中。

## 历史版本

PCKB 采用持续迭代的预览版发布方式。旧版本保留用于回退与历史参考。

- [v0.7.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.7.0) — Mac AI Workbench V1 首版；保留用于回退
- [v0.6.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0) — macOS 与 Windows 11 x64 历史版本；Windows 用户继续使用此版本
- [v0.5.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.5.0) — 较早公开预览版本
- [v0.4.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.4.0) — 首个公开预览版本
- [v0.3.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.3.0) — AI 多 Provider 版本
- [v0.2.2](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.2) — 问题反馈流程更新
- [v0.2.1](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.1) — 先前公开版本
- [v0.1.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.1.0) — 首个公开版本

Mac 新安装请使用 [PCKB 0.7.1 Public Preview](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.7.1)；Windows 用户继续使用历史 [v0.6.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0)。

## 许可

PCKB 应用不是开源软件。安装与使用受 [EULA](legal/PCKB-EULA.txt) 约束，下载包内也会包含该文件。第三方声明单独提供，并且不会削弱第三方开源许可证授予的权利。
