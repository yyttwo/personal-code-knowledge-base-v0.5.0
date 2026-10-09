# PCKB 0.7.0 Public Preview 隐私说明

个人代码资产库采用 Local-first 设计。代码库、资产 Project、学习记录、普通搜索索引、语义索引和备份保存在本机。代码库位置由用户选择；AI Workbench 的会话、工作副本及相关历史保存在 App 的本机应用数据中。

本次 v0.7.0 仅发布 macOS Apple Silicon 版本。历史 Windows v0.6.0 继续保留，但不包含此次全部 AI Workbench 功能。既有资产 AI 辅助可以选择本机 Ollama 或用户配置的 DeepSeek / Qwen；新版工作台独立配置 DeepSeek 或 Qwen，未配置时不会自动借用其他 Provider。

## 本机处理

App 不包含 Telemetry、Analytics、Cloud Sync、远程 Crash Upload 或代码执行。普通搜索、结构化筛选、Secret 风险提示、重复检查、备份与恢复都在本机完成。

Library 的普通代码库文件是正式资产数据来源，搜索索引可以重建。AI Workbench 则另有用于持久保存会话、工作副本和恢复信息的本地数据库；这些工作台数据不是可随意删除的搜索缓存。不要为重建搜索索引而删除工作台应用数据。

## AI Provider 与网络请求

只有用户明确配置 Provider / 模型并主动执行 AI 操作时，App 才会发起对应请求；用户主动点击连接测试等设置操作也会访问所选服务。打开本地会话历史、普通关键词搜索或检查重复代码不会自动发起云端生成请求。

- **Ollama：** 请求发送到用户配置的本机回环地址。
- **DeepSeek：** Generation 与 AI Chat 请求发送到用户配置的 DeepSeek API 地址，默认地址为 `https://api.deepseek.com`。
- **Qwen：** Generation、AI Chat 或 Embedding 请求发送到用户配置的千问 AI 平台地址，默认地址为 `https://maas.qianwenaiapi.com/compatible-mode/v1`。

既有 Generation Provider 与 Embedding Provider 相互独立。资产 AI 内容辅助使用保存的 Generation Provider；语义索引与智能搜索使用保存的 Embedding Provider。AI Workbench V1 使用单独保存的 DeepSeek / Qwen 设置和受支持的模型配置，不会自动回退到其他云端 Provider。

使用 DeepSeek 或 Qwen 时，完成当前请求所需的代码或文字会发送给相应第三方服务商，并受其服务条款与隐私政策约束。App 会在发送前执行 Secret 风险检查与脱敏保护，但这不是完整的安全审计；请勿提交真实凭据、私钥或不适合交给第三方的代码。

使用 Qwen API 建立语义索引时，需要把待索引资产的相关文本分段发送到 Qwen Embedding 服务。索引向量及激活状态仍保存在本机。

## AI Workbench 的上下文边界

Ask、Code、Project 和 Learning 请求会把完成用户所选任务所需的问题、代码、需求或选定历史上下文发送给工作台 Provider。导入代码只创建本地工作副本，不会改写原始文件；在用户主动请求 AI 分析或修改时，相应代码内容才成为请求的一部分。

“＋ PCKB 知识”的普通本地搜索不会上传整个代码库。用户明确选中的资产快照会作为本次上下文发送，未选中资产和未选中附件不会因为搜索而自动发送。历史回答的参考来源绑定当时选定的快照，不会随资产后来修改而自动替换。

从旧本机 Ollama 会话继续到云端 Provider 时，App 会先提示数据边界；用户可以只发送新问题、选择包含历史上下文继续，或取消。打开历史本身不会向云端发送其内容。

“保存到 PCKB”是在用户查看预览并确认后，通过本机代码库接口新建资产并检查重复；不会自动覆盖已有资产。更新已有资产仍通过“全部资产 → 编辑”完成。Code 应用与撤销只作用于工作台副本；Project 导出由用户选择目标，不会自动执行生成代码或覆盖外部开发项目。

## API Key

本次 Mac 版本的 DeepSeek / Qwen API Key 由可信后端通过 macOS 钥匙串保存和读取；不会回填到前端输入框，不写入代码库、搜索索引、工作台数据库、备份或普通配置文件。设置界面只显示凭据是否已配置；更新输入框为空。历史 Windows v0.6.0 的 API Key 使用 Windows Credential Manager。

删除 App 不一定会自动删除系统凭据。用户可以先在 App 设置中删除 API Key，或之后通过 macOS“钥匙串访问”或 Windows“凭据管理器”管理相应项目。

## App 可以访问哪些文件

除 App 自己的本机应用数据外，文件操作围绕用户通过系统文件选择器明确选择的位置工作：

- 当前代码库文件夹；
- 用户主动选择的单个导入文件；
- 用户选择的备份保存位置；
- 用户选择的恢复备份。
- 用户为 App 背景明确选择的本机图片。
- 用户在工作台导出时明确选择的目标位置。

App 不自动扫描整个 Home 目录，也不自动扫描项目文件夹。

自定义 App 背景保存在本机，不会发送给 AI Provider。

## 单文件导入与 Sensitive Guardrail

导入时，App 对所选文件进行只读检查和读取，不修改、删除、重命名或执行源文件。保存成功后，代码副本进入用户自己的代码库。

App 会阻止明显的凭据文件名，并对普通代码中看起来像 Secret 的片段给出警告或脱敏保护。这些检查不能保证代码中没有任何 Secret，保存、发送给 AI、分享或备份前仍应由用户检查内容并撤销已经暴露的真实凭据。

## 备份与恢复

本地备份可能包含完整代码、笔记、来源、验证记录、废纸篓和 Project 关系。App 不会对备份额外加密，请将备份保存在受信任的位置，并使用系统磁盘加密、访问控制或离线保管。

Library 备份不等同于全部 App 应用数据备份，也不会自动包含全部 AI Workbench 会话与工作副本历史。工作台会话移入会话废纸篓后仍可恢复；不要将其与资产废纸篓或可重建索引混淆。

## 权限与发布范围

0.7.0 Public Preview 不申请摄像头、麦克风、位置、联系人、日历或屏幕录制权限。文件访问由用户在系统选择器中的明确操作限定。

0.7.0 Public Preview 仅面向 Apple Silicon Mac（macOS 11.0 或更高版本），采用个人本地安装方式，不提供 Windows 新安装包。历史 Windows 11 x64 v0.6.0 仍可从旧 Release 下载。正式下载由本仓库的 GitHub Release 页面提供；目前不提供 Mac App Store 版本、自动更新、Intel Mac 或 Windows ARM64 兼容保证。
