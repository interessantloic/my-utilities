# 新 Mac 换机清单

## 准备与安装

- [ ] 安装 [Homebrew](https://brew.sh/)，完成安装器提示的 shell 环境配置。
- [ ] 下载或克隆本仓库，在终端进入仓库根目录。
- [ ] 查看 `Brewfile`，确认需要安装的工具。
- [ ] 执行 `brew bundle --file=Brewfile`。
- [ ] 执行 `brew bundle check --file=Brewfile`，确认安装清单的依赖已满足。

## 首次设置

- [ ] 按[个人应用说明](personal-apps.md)手动安装 SyncClipboard。
- [ ] KeyCastr：按系统提示允许输入监控，验证按键显示。
- [ ] Keka：用测试压缩包确认压缩和解压正常。
- [ ] Snipaste：允许截图所需权限，设置并测试截图、贴图快捷键。
- [ ] Paste：完成账号／订阅恢复，测试非敏感文本的历史记录。
- [ ] SyncClipboard：私下填写服务器与认证信息，用测试文本验证同步。
- [ ] Cockpit Tools：按需重新登录所用服务，确认账号与配额显示。

- [ ] 打开 Syntax Highlight 一次。
- [ ] 在系统设置的 Quick Look（快速查看）扩展列表中启用 Syntax Highlight。
- [ ] 在 Finder 中选中一个包含文本的 `.yaml` 文件，按空格确认能看到内容。
- [ ] 如需预览 `.env`，使用不含密码的测试文件验证；在 Finder 中可用 `Command + Shift + .` 显示隐藏文件。
- [ ] `.pub` 文件另行验证，不把安装成功视为所有文件格式均已支持。

具体操作和排查见 [Syntax Highlight](syntax-highlight.md)。系统设置入口会随 macOS 版本变化，可搜索 “Quick Look” 或“快速查看”。

## 日常维护

新增工具时同步更新 README、Brewfile 和工具说明。只收录希望在下一台电脑上继续使用的工具；软件已安装不代表已完成首次设置。

应用登录、商业许可证及个人配置通过各自的安全备份方式迁移。不要把私人配置直接上传到此公开仓库。
