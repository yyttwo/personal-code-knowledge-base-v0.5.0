# PCKB

Personal Code Knowledge Base

Turn the code you write, learn, and collect into a searchable personal knowledge base — with local or cloud AI.

[简体中文](README.md) | [English](README.en.md)

**Public Preview · macOS Apple Silicon · Windows 11 x64 · Simplified Chinese + English**

PCKB helps you keep code you have written, useful implementations from projects, and examples collected while learning. Store code together with its purpose, notes, tags, Projects, and learning records. Find it again with keywords and structured filters, or configure an embedding model for semantic search when you remember the idea but not the name.

You can use it as a local code knowledge base first and enable AI explanations, suggestions, or chat when needed. Core library management, keyword search, learning, backups, and Trash do not require AI. macOS and Windows share the same product interface, and libraries stay in a folder you choose; cloud AI is an optional user-selected enhancement.

PCKB is under active development. This repository is the public binary release repository; it does not contain the product's core source code.

## Download

**Recommended for new users:** [PCKB 0.6.0 Public Preview](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0).

### macOS

Apple Silicon / arm64, macOS 11.0 or later: [PCKB-0.6.0-Public-Preview-macOS-arm64.zip](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-macOS-arm64.zip).

The macOS build is ad hoc signed, **not** Apple Developer ID signed or notarized. See [INSTALL_MACOS.md](INSTALL_MACOS.md).

### Windows

Windows 11 / x64: [PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe).

The NSIS installer is **not** Authenticode signed, so SmartScreen may warn about an unknown publisher. See [INSTALL_WINDOWS.md](INSTALL_WINDOWS.md). Verify either download against `SHA256SUMS.txt` in the same release.

![PCKB Main Library and Code Detail](screenshots/public/en/01-main-library.png)

The images below are real PCKB screenshots from a synthetic demo library. Personal local paths are covered with opaque rectangles; no product controls or other content were changed.

Current product screenshots are from the macOS build; the Windows build uses the same PCKB product UI and core workflows.

## Features

- Complete Simplified Chinese and English interfaces, with System language selection and instant in-app switching
- Personal code library with Projects, tags, favorites, learning status, and validation history
- Full-text and structured search
- Optional semantic/hybrid search and related-code discovery
- Safe single-file import, recoverable Trash, and local backup/restore
- AI code actions and AI Chat
- Custom App backgrounds stored locally

## Screenshots

### Capture and organize

| Create a code asset | Manage a project |
| --- | --- |
| ![New asset editor](screenshots/public/en/02-new-asset.png) | ![Project management](screenshots/public/en/10-project-management.png) |

### Learn and review

| Learning overview | Asset learning cards |
| --- | --- |
| ![Learning Center overview](screenshots/public/en/03-learning-overview.png) | ![Learning Center asset cards](screenshots/public/en/08-learning-assets.png) |

### Search, configure, and safeguard

| General and AI settings | Semantic search settings |
| --- | --- |
| ![General and AI settings](screenshots/public/en/05-general-settings.png) | ![Semantic search settings](screenshots/public/en/06-semantic-search-settings.png) |

| Trash | Feedback and privacy guidance |
| --- | --- |
| ![Recoverable Trash](screenshots/public/en/04-trash.png) | ![Feedback and privacy guidance](screenshots/public/en/11-feedback.png) |

### Optional AI Chat

![AI Chat](screenshots/public/en/09-ai-chat.png)

### Make it yours

![Local App background settings](screenshots/public/en/07-app-background.png)

## AI options

- **Ollama:** optional local Generation and Embedding workflows
- **DeepSeek API:** optional BYOK Generation and AI Chat
- **Qwen API:** optional BYOK Generation, AI Chat, and Embedding
- Generation and Embedding providers are configured independently
- API credentials use macOS Keychain on Mac and Windows Credential Manager on Windows
- There is no automatic cloud-provider fallback

Cloud AI operations send the content required for the user-requested operation to the selected provider. See [PRIVACY.md](PRIVACY.md).

The App includes the built-in PCKB night-lake background. You can choose a local image and adjust its overlay, blur, and Cover/Contain display mode; the background image remains on the Mac.

## Quick Start

1. Download the macOS ZIP or Windows installer above and verify its SHA-256.
2. Follow the [macOS](INSTALL_MACOS.md) or [Windows](INSTALL_WINDOWS.md) installation guide.
3. Open PCKB and create or open a local library.

Windows users can follow the [download, installation, and first-use guide](INSTALL_WINDOWS.md). Start by saving one code asset with its purpose and tags, then try search, Project organization, and learning status. Configure Ollama, DeepSeek, or Qwen later if you want AI assistance.

## Privacy

The library is primarily stored in ordinary files at a local folder selected by the user. Ollama supports local AI workflows. DeepSeek and Qwen are optional external BYOK providers. PCKB does not automatically fall back to another cloud provider.

## Documentation

- [macOS installation](INSTALL_MACOS.md)
- [Windows installation](INSTALL_WINDOWS.md)
- [User guide](USER_GUIDE.md)
- [Privacy](PRIVACY.md)
- [Security](SECURITY.md)
- [Source-code status](SOURCE_CODE_NOTICE.md)

## Legal

PCKB is distributed as proprietary freeware under the [PCKB EULA](legal/PCKB-EULA.txt). Downloading, installing, or using PCKB is subject to that EULA. Third-party open-source components remain subject to their own licenses. See the [Third-Party Notices](legal/THIRD-PARTY-NOTICES.txt), [component source references](legal/OPEN-SOURCE-COMPONENT-SOURCES.md), and [open-source license bundle](legal/OPEN-SOURCE-LICENSES/).

## Known limitations

- macOS: Apple Silicon (arm64) only; no Apple Developer ID signature or notarization. Intel Mac is not supported.
- Windows: Windows 11 x64 only; the installer is unsigned and SmartScreen may warn. Windows 10 and ARM64 are not supported targets.
- No cloud sync, automatic updates, folder batch import, Git/GitHub sync, VS Code extension, or code execution.
- Ollama models must be installed and managed separately. DeepSeek and Qwen require the user's own API key, network access, and service quota.
- This is an active-development Public Preview, not a stable or feature-complete release.

## Previous Releases

PCKB follows an iterative preview release model. Older versions remain available for rollback and historical reference.

- [v0.5.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.5.0) — Previous public preview
- [v0.4.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.4.0) — First public preview
- [v0.3.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.3.0) — AI Multi-Provider release
- [v0.2.2](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.2) — Feedback workflow update
- [v0.2.1](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.1) — Previous public release
- [v0.1.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.1.0) — Initial public release

For new installations, use [PCKB 0.6.0 Public Preview](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0) unless you specifically need an older version.

## License

The PCKB application is not open source. Installation and use are governed by the [EULA](legal/PCKB-EULA.txt), which is also included with the download. Third-party notices are provided separately and do not reduce rights granted by third-party open-source licenses.
