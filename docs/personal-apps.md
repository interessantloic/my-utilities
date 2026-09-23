# 个人小应用：安装与首次设置

以下应用记录用途、官方下载和换机步骤。团队自制快捷操作及其 FFmpeg、ImageMagick、Python 依赖不在这个公开仓库中。

## KeyCastr

把键盘按键显示到屏幕上，方便录屏、演示和协作。

```bash
brew install --cask keycastr
open -a KeyCastr
```

按系统提示在“隐私与安全性”中允许输入监控；必要时重新启动应用。按几个普通快捷键，确认屏幕上出现按键显示，再按需调整位置与样式。

来源：[官方项目及权限说明](https://github.com/keycastr/keycastr)、[Homebrew](https://formulae.brew.sh/cask/keycastr)。

## Keka

用于日常文件压缩与解压。

```bash
brew install --cask keka
```

首次打开后按习惯设置解压位置。用一组测试文件压缩再解压，检查文件是否完整；默认打开方式按需设置。

来源：[官网](https://www.keka.io/)、[Homebrew](https://formulae.brew.sh/cask/keka)。

## Snipaste

截图并把图片贴在桌面上作为参考。

```bash
brew install --cask snipaste
```

首次打开后按提示允许截图所需的系统权限，检查截图和贴图快捷键是否与其他应用冲突。截取一块桌面区域并贴图验证。

来源：[官网](https://www.snipaste.com/)、[Homebrew](https://formulae.brew.sh/cask/snipaste)。

## Paste

保存和检索剪贴板历史。

```bash
brew install --cask paste
```

完成应用内账号与订阅恢复；用无敏感信息的文本测试复制、历史检索和粘贴。历史记录与登录数据不保存到此仓库。

来源：[官网](https://pasteapp.io/)、[Homebrew](https://formulae.brew.sh/cask/paste)。

## SyncClipboard

用于跨设备剪贴板同步和历史记录管理。

1. 在[官方 Releases](https://github.com/Jeric-X/SyncClipboard/releases)下载适合当前 Mac 架构的 macOS 安装包。
2. 安装并启动应用，参照[官方 macOS 说明](https://github.com/Jeric-X/SyncClipboard#macos)。
3. 根据自己的部署方式，设置独立服务器、WebDAV 或其他支持的后端。
4. 使用非敏感测试文本验证双向同步。

此应用采用手动安装，不写入未经确认的 Homebrew 包名。服务器地址、账号和密码通过私下配置恢复。

## Cockpit Tools

管理 AI 工具的多个账号、配额和实例。

```bash
brew tap jlcodes99/cockpit-tools https://github.com/jlcodes99/cockpit-tools
brew install --cask cockpit-tools
```

Brewfile 已包含上述 tap 和 cask。启动后仅配置实际使用的服务，并通过应用支持的流程重新登录。若系统阻止打开，先核对官方版本和系统提示，再参照上游安装说明处理。

账号导出文件、OAuth Token 和 API Key 不保存到此仓库。应用的使用范围与许可证以官方说明为准。

来源：[官方项目与安装说明](https://github.com/jlcodes99/cockpit-tools#安装指南-installation)。
