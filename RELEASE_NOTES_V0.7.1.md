# PCKB 0.7.1 Public Preview

**macOS Apple Silicon Only（arm64，macOS 11.0+）。本次没有 Windows 新安装包。**

## 修复

- 修复 AI 工作台历史会话 `⋯` 菜单重叠、残留和被滚动列表边缘裁切的问题。
- 同时最多显示一个菜单；打开其他会话菜单时自动关闭之前的菜单。
- 菜单按窗口可用空间定位，避免遮住相邻会话操作入口；窄窗口及列表底部仍可操作。
- 点击外部、按 Esc、切换会话、滚动列表及调整窗口时正确关闭菜单。
- 重命名、移到会话废纸篓及恢复行为保持不变。

这是 v0.7.0 的 UI 修复补丁，没有新增 AI 功能、依赖、SQLite 或 Library 格式变更。PCKB 不会自动执行生成代码，OpenCodeReview 不属于本次发布内容。

## 安装与升级

下载 `PCKB-0.7.1-Public-Preview-macOS-arm64.zip` 和 `SHA256SUMS.txt`，核对 SHA-256 后解压，将 `PCKB.app` 放到“应用程序”。更新前退出旧 App，保留原有代码库及正常备份；不要删除 Library 来更新 App。

使用 ad hoc 签名，**没有 Apple Developer ID 签名或 Apple 公证**。系统提示的处理方式见 [INSTALL_MACOS.md](INSTALL_MACOS.md)，不要关闭系统安全保护。

历史 Mac v0.7.0 和 Windows v0.6.0 保留下载与回退能力。Windows v0.6.0 不包含新版 Mac 的全部 AI Workbench 功能。

## English

PCKB 0.7.1 Public Preview is a macOS Apple Silicon (arm64, macOS 11.0+) UI patch. It fixes overlapping, lingering, and clipped Workbench session menus. Only one menu is open at a time; menu positioning and dismissal work across scrolling and window sizes. Rename, Session Trash, and restore remain unchanged.

Verify the ZIP against `SHA256SUMS.txt`, extract `PCKB.app`, and place it in Applications. Quit the old App before upgrading and keep your external Library and backups. The App is ad hoc signed, not Developer ID signed or notarized. No Windows installer is provided; historical Windows v0.6.0 remains available.
