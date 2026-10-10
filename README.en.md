# PCKB

Personal Code Knowledge Base

Turn the code you write, learn, and collect into a searchable personal knowledge base — with local or cloud AI.

[简体中文](README.md) | [English](README.en.md)

**PCKB 0.7.1 Public Preview · macOS Apple Silicon Only · Simplified Chinese + English**

**v0.7.1 ships only for macOS Apple Silicon (arm64). No new Windows installer is provided.** The historical Windows v0.6.0 download remains available; it does not include all of the new AI Workbench features in this Mac release.

## Download

**[PCKB 0.7.1 Public Preview — macOS Apple Silicon Only](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.7.1)**

| Platform | Requirements | Download |
| --- | --- | --- |
| macOS · v0.7.1 | Apple Silicon arm64 · macOS 11.0+ | [macOS ZIP](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.1/PCKB-0.7.1-Public-Preview-macOS-arm64.zip) |
| Windows · historical v0.6.0 | Windows 11 x64 | [Historical Windows installer](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe) |

Verify the new Mac ZIP against [v0.7.1 SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.1/SHA256SUMS.txt). Verify the historical Windows installer against [v0.6.0 SHA256SUMS.txt](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/SHA256SUMS.txt). GitHub's automatic Source code archives contain this downloads/documentation repository, not PCKB application source.

PCKB helps you keep code you have written, useful implementations from projects, and examples collected while learning. Store code together with its purpose, notes, tags, Projects, and learning records. Find it again with keywords and structured filters, or configure an embedding model for semantic search when you remember the idea but not the name.

You can use it as a local code knowledge base first and enable AI explanations, suggestions, or the Workbench when needed. Core library management, keyword search, asset learning records, backups, and Trash do not require AI. Libraries stay in a folder you choose; cloud AI is an optional user-selected enhancement. AI Workbench V1 is new to Mac v0.7.1 and is not a claim of feature parity with historical Windows v0.6.0.

PCKB is under active development. This repository is the public binary release repository; it does not contain the product's core source code.

### macOS — Apple Silicon

Apple Silicon / arm64, macOS 11.0 or later: [PCKB-0.7.1-Public-Preview-macOS-arm64.zip](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.7.1/PCKB-0.7.1-Public-Preview-macOS-arm64.zip).

The macOS build is ad hoc signed, **not** Apple Developer ID signed or notarized. See [INSTALL_MACOS.md](INSTALL_MACOS.md).

Download the ZIP, run `shasum -a 256 PCKB-0.7.1-Public-Preview-macOS-arm64.zip`, compare the hash, extract `PCKB.app`, and drag it into Applications. Only after verifying the official source and hash, use Finder → Applications → Control-click PCKB → Open → confirm Open if offered; otherwise use System Settings → Privacy & Security → Open Anyway. Do not disable system protection. Quit the old App before replacing it for an update; keep your external Library. See the installation guide for detailed steps and Apple's safety guidance.

### Windows 11 x64 — historical v0.6.0

Windows 11 / x64: [PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/download/v0.6.0/PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe).

There is no Windows v0.7.1 installer. The v0.6.0 download and installation guide remain available. That NSIS installer is **not** Authenticode signed, so SmartScreen may warn about an unknown publisher. See [INSTALL_WINDOWS.md](INSTALL_WINDOWS.md) and use `SHA256SUMS.txt` from v0.6.0 for this Windows file.

Download Setup.exe and run `Get-FileHash ".\PCKB-0.6.0-Public-Preview-Windows-x64-Setup.exe" -Algorithm SHA256`. Expected hash: `27fce8290fd42bfd9a6ec7bdf37b44179012e9a505469522ccfc1c6ca76b7a55`. Only after confirming the official source and hash, use More info → Run anyway if SmartScreen warns. Never disable Defender or SmartScreen. If Already Installed appears, choose Uninstall before installing and leave Delete the application data unchecked. Keep the installer default location. On the completion page, Run PCKB may stay selected; Create desktop shortcut is optional. Click Finish. If Microsoft Edge WebView2 Runtime is not already available, the installer may need network access to obtain the required runtime. Keep normal backups of your external Library.

![PCKB Main Library and Code Detail](screenshots/public/01-main-library.png)

The images below are real PCKB screenshots from a synthetic demo library. Personal local paths are covered with opaque rectangles; no product controls or other content were changed.

These approved screenshots are from an earlier macOS version and illustrate existing library features, not the full new AI Workbench. Historical Windows v0.6.0 retains its original core library features; the new Mac Workbench features should not be assumed to exist in that Windows release.

## v0.7.1 fix

- Fix overlapping, lingering, and clipped Workbench session action menus.
- Only one menu is open at a time; outside clicks, Esc, scrolling, window resizing, and session changes dismiss it correctly.
- Rename, Session Trash, and restore remain unchanged. No new AI features or database format changes.

## Features

- Complete Simplified Chinese and English interfaces, with System language selection and instant in-app switching
- Personal code library with Projects, tags, favorites, learning status, and validation history
- Full-text and structured search
- Optional semantic/hybrid search and related-code discovery
- Safe single-file import, recoverable Trash, and local backup/restore
- AI code actions and the new AI Workbench V1 in Mac v0.7.0
- Custom App backgrounds stored locally

## AI Workbench V1 — Mac v0.7.0

- **Ask:** AI questions and conversation.
- **Code:** find problems, explain code, and preview proposed changes; explicitly apply them to a local working copy, undo, and copy the code.
- **Project:** requirements → plan → file generation → review → folder or source ZIP export.
- **Learning:** graded hints, explanation before code, reference answers, and student-code review.
- **PCKB Knowledge:** explicitly select existing code assets as AI context and inspect their reference sources in the answer.
- **Save to PCKB:** preview and create a new asset, with identical-code detection to avoid duplicates. Update existing assets through All Assets → Edit instead.
- Recover deleted Workbench sessions through Session Trash. This release also improves code-language detection, Markdown tables, and code-review filenames.

The Workbench has independently saved DeepSeek or Qwen provider/model settings. Cloud features require the user's own supported API key. Changes do not automatically overwrite original files, and PCKB **does not execute generated code**. Copy or export it to your own development environment for review and execution.

OpenCodeReview deep project review is not included in this release.

## Screenshots

### Capture and organize

| Create a code asset | Manage a project |
| --- | --- |
| ![New asset editor](screenshots/public/02-new-asset.png) | ![Project management](screenshots/public/03-project-management.png) |

### Learn and review

| Learning overview | Asset learning cards |
| --- | --- |
| ![Learning Center overview](screenshots/public/04-learning-overview.png) | ![Learning Center asset cards](screenshots/public/05-learning-assets.png) |

### Configure and safeguard

| AI and semantic search settings | Backup and restore |
| --- | --- |
| ![AI settings](screenshots/public/06-ai-settings.png) | ![Backup and restore](screenshots/public/07-backup-restore.png) |

### Make it yours

![Local App background settings](screenshots/public/08-app-background.png)

The retained screenshot set covers existing library, settings, and appearance workflows. See the Workbench overview above and the [user guide](USER_GUIDE.md) for the new workflows.

## AI options

- **Ollama:** optional local Generation and Embedding workflows
- **DeepSeek API:** optional BYOK Generation and AI Chat
- **Qwen API:** optional BYOK Generation, AI Chat, and Embedding
- Generation and Embedding providers are configured independently
- AI Workbench V1 uses separate DeepSeek / Qwen settings and does not automatically switch to another provider
- API credentials use macOS Keychain on Mac and Windows Credential Manager on Windows
- There is no automatic cloud-provider fallback

Cloud AI operations send the content required for the user-requested operation to the selected provider. See [PRIVACY.md](PRIVACY.md).

The App includes the built-in PCKB night-lake background. You can choose a local image and adjust its overlay, blur, and Cover/Contain display mode; the background image remains on your computer.

## Quick Start

1. For the new Mac release, download v0.7.1; for Windows, use historical v0.6.0. Verify against the matching release's SHA-256 file.
2. Follow the [macOS](INSTALL_MACOS.md) or [historical Windows](INSTALL_WINDOWS.md) installation guide.
3. Open PCKB and create or open a local library.

Windows users can follow the [historical v0.6.0 download, installation, and first-use guide](INSTALL_WINDOWS.md). Start by saving one code asset with its purpose and tags, then try search, Project organization, and learning status. On Mac, configure the new Workbench provider, model, and API credentials under Settings → AI Workbench when needed.

## Privacy

The library is primarily stored in ordinary files at a local folder selected by the user. Ollama supports local AI workflows. DeepSeek and Qwen are optional external BYOK providers. PCKB does not automatically fall back to another cloud provider.

## Documentation

- [v0.7.1 release notes](RELEASE_NOTES_V0.7.1.md)
- [v0.7.0 release notes](RELEASE_NOTES_V0.7.0.md)
- [macOS installation](INSTALL_MACOS.md)
- [Windows installation](INSTALL_WINDOWS.md)
- [User guide](USER_GUIDE.md)
- [Privacy](PRIVACY.md)
- [Security](SECURITY.md)
- [Source-code status](SOURCE_CODE_NOTICE.md)

## Updates

PCKB Public Preview currently does not include automatic updates. New versions should be downloaded from the [official GitHub Releases page](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases).

PCKB 0.7.1 is a macOS Apple Silicon-only Public Preview. The product is still under active development; a new Windows release has not been published.

PCKB is local-first. Your Library stays under your control. Optional AI features may use the provider you configure. PCKB application source code is currently private. This public repository is used for official downloads, documentation, screenshots, and release information.

## Legal

PCKB is distributed as proprietary freeware under the [PCKB EULA](legal/PCKB-EULA.txt). Downloading, installing, or using PCKB is subject to that EULA. Third-party open-source components remain subject to their own licenses. See the [Third-Party Notices](legal/THIRD-PARTY-NOTICES.txt), [component source references](legal/OPEN-SOURCE-COMPONENT-SOURCES.md), and [open-source license bundle](legal/OPEN-SOURCE-LICENSES/).

## Known limitations

- macOS: Apple Silicon (arm64) only; no Apple Developer ID signature or notarization. Intel Mac is not supported.
- No Windows v0.7.1 is provided. Historical Windows v0.6.0 targets Windows 11 x64 only; its unsigned installer may trigger SmartScreen. Windows 10 and ARM64 are not supported targets.
- No cloud sync, automatic updates, folder batch import, Git/GitHub sync, VS Code extension, or code execution.
- Ollama models must be installed and managed separately. DeepSeek and Qwen require the user's own API key, network access, and service quota.
- This is an active-development Public Preview, not a stable or feature-complete release.
- OpenCodeReview deep project review is not included.

## Previous Releases

PCKB follows an iterative preview release model. Older versions remain available for rollback and historical reference.

- [v0.7.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.7.0) — initial Mac AI Workbench V1 release; retained for rollback
- [v0.6.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0) — Historical macOS and Windows 11 x64 release; the current download for Windows users
- [v0.5.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.5.0) — Earlier public preview
- [v0.4.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.4.0) — First public preview
- [v0.3.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.3.0) — AI Multi-Provider release
- [v0.2.2](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.2) — Feedback workflow update
- [v0.2.1](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.1) — Previous public release
- [v0.1.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.1.0) — Initial public release

For new Mac installations, use [PCKB 0.7.1 Public Preview](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.7.1). Windows users should continue to use historical [v0.6.0](https://github.com/yyttwo/personal-code-knowledge-base-v0.5.0/releases/tag/v0.6.0).

## License

The PCKB application is not open source. Installation and use are governed by the [EULA](legal/PCKB-EULA.txt), which is also included with the download. Third-party notices are provided separately and do not reduce rights granted by third-party open-source licenses.
