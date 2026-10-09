# PCKB 0.7.0 Public Preview：macOS 安装说明

**macOS Apple Silicon Only。本次 v0.7.0 不提供 Windows 安装包。** 历史 Windows v0.6.0 仍可下载，见 [Windows 安装说明](INSTALL_WINDOWS.md)。

## 系统要求

- Apple Silicon Mac（arm64）
- macOS 11.0 或更高版本

当前安装包不支持 Intel Mac。

## 安装步骤

1. 从 [v0.7.0 Release](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.7.0) 下载 `PCKB-0.7.0-Public-Preview-macOS-arm64.zip` 和 `SHA256SUMS.txt`。
2. 核对 ZIP 的 SHA-256 与 `SHA256SUMS.txt` 一致。
3. 在 Finder 中双击 ZIP 解压。
4. 将 `PCKB.app` 拖到“应用程序”文件夹。
5. 在“应用程序”中打开 PCKB。
6. 第一次启动时，选择“创建新的代码库”并指定一个空文件夹；已有代码库请选择“打开已有代码库”。

代码库是用户自己的数据。建议放在容易找到、管理和备份的位置。删除或替换 App 不会自动删除代码库。

## 首次打开时的 macOS 提示

0.7.0 Public Preview 使用 ad hoc 签名，没有 Developer ID 签名或 Apple 公证。macOS 因此可能显示“无法验证开发者”或等价提示。

请先确认下载来源和 SHA-256。若 macOS 阻止首次启动，只使用系统提供的图形界面流程：

1. Finder → Applications / 应用程序 → PCKB → 按住 Control 点击 / 右键 → Open / 打开 → 再确认打开（如果此系统版本提供该选项）；或
2. 尝试打开后，打开“系统设置”→“隐私与安全性”→“仍要打开”，再确认“打开”。

仅在文件来自官方 PCKB Release、SHA256 完全匹配且你信任此来源时操作。校验匹配证明文件与发布物一致，不代替 Apple 的安全审核；若提示已知恶意软件或文件损坏，请停止并反馈。

本文不建议关闭 Gatekeeper、停用系统安全保护或运行命令行绕过操作。

不同 macOS 版本的文字可能略有差异；请以 Apple 的[安全打开 Mac App 说明](https://support.apple.com/102445)为准。

## SHA-256 校验

macOS 终端可使用：

```sh
shasum -a 256 PCKB-0.7.0-Public-Preview-macOS-arm64.zip
```

预期结果必须与 [v0.7.0 Release 的 SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.0/SHA256SUMS.txt) 中公布的值完全一致。不要使用历史 v0.6.0 的校验值核对新版 ZIP。

若不一致，请停止安装并重新从正式 Release 页面下载。

## 从旧版本升级

1. 在旧版本中创建一次有效备份。
2. 退出旧 App。
3. 用 0.7.0 Public Preview 的 `PCKB.app` 替换“应用程序”中的旧版本。
4. 启动 PCKB，并打开原来的代码库。
5. 检查资产与 Project；如启用语义搜索，根据设置中的提示重新构建语义索引。

代码库位于用户选择的独立文件夹中，升级、重装或删除 App 不应自动删除代码库。API Key 保存在 macOS 钥匙串中，不属于代码库备份。

PCKB Public Preview 当前不包含自动更新。新版本请从官方 GitHub Releases 页面重新下载安装；不要删除外部 Library 来完成更新，并对重要代码资产保持正常备份。

## AI Workbench 初次配置

打开代码库后，进入“设置 → AI 工作台”，选择受支持的 DeepSeek 或 Qwen Provider / 模型，配置自己的 API Key 并保存。凭据由可信后端保存在 macOS 钥匙串中；更新 Key 的输入框不会回填已有 Key。系统若要求钥匙串权限，请由用户通过正常系统窗口处理。

工作台的 Ask、Code、Project 和 Learning 会使用这里保存的配置。资产库管理不要求开启工作台；PCKB 不会自动执行生成的代码，也不会为了工作台修改你的外部开发项目。

## English installation summary

PCKB 0.7.0 Public Preview supports Apple Silicon arm64 on macOS 11.0 or later only. Download the v0.7.0 ZIP and its matching `SHA256SUMS.txt`, verify the hash, extract `PCKB.app`, and drag it into Applications. Quit the previous App before replacing it, and retain your external Library and normal backups.

The App is ad hoc signed, not Apple Developer ID signed or notarized. If macOS blocks first launch, use its normal Finder Open or Privacy & Security → Open Anyway workflow only after verifying the official source and checksum. Do not disable Gatekeeper or other system protection. The historical Windows v0.6.0 release remains available; there is no Windows v0.7.0 installer.
