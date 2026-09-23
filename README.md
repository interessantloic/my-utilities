# my-utilities

我的实用工具收藏与 Mac 换机手册。记录每个工具解决的问题、官方来源、安装方式和安装后的必要设置，让下次换电脑时可以快速恢复熟悉的工作环境。

Personal utilities, setup notes, and a Homebrew install list for setting up a new Mac.

## 工具目录

| 工具 | 用途 | 安装方式 | 使用说明 |
| --- | --- | --- | --- |
| [Syntax Highlight](https://github.com/sbarex/SourceCodeSyntaxHighlight) | 在 Finder 中按空格预览 YAML、源码及部分无扩展名文本 | `brew install --cask syntax-highlight` | [安装与排查](docs/syntax-highlight.md) |

## 新 Mac 快速开始

1. 按 [Homebrew 官网](https://brew.sh/)的说明安装 Homebrew，并完成安装器提示的终端环境配置。
2. 在本仓库页面选择 **Code → Download ZIP**，解压后在终端进入该文件夹。也可以使用 **Code** 菜单中的 HTTPS 地址执行 `git clone`。
3. 在仓库根目录执行：

   ```bash
   brew bundle --file=Brewfile
   ```

4. 按照[换机清单](docs/new-mac.md)完成首次启动、扩展启用和功能验证。

`brew bundle` 会安装缺少的软件，并默认尝试升级已有软件。只想补齐缺少的软件时，使用 `brew bundle --file=Brewfile --no-upgrade`。此清单不锁定版本，也不恢复登录状态或应用配置。详见 [Homebrew Bundle 文档](https://docs.brew.sh/Brew-Bundle-and-Brewfile)。

## 仓库内容

```text
my-utilities/
├── README.md                 # 工具索引与入门说明
├── Brewfile                  # 可批量安装的工具
├── .gitignore                # 排除本机文件和常见敏感配置
└── docs/
    ├── new-mac.md            # 换机检查清单
    ├── syntax-highlight.md   # Finder 文本预览工具
    └── tool-template.md      # 新工具记录模板
```

## 添加新工具

1. 复制 `docs/tool-template.md` 为工具自己的说明文件，写清用途、官方来源、安装方式和验证步骤。
2. 在上方工具目录添加一行。
3. 如果支持 Homebrew，将经过确认的包名加入 `Brewfile`：GUI 应用使用 `cask "包名"`，命令行工具使用 `brew "包名"`。
4. 提交前检查变更，确保只有打算公开的内容。

## 公开内容约定

这里保存工具说明、安装清单和可公开的配置示例。密码、API Token、SSH 私钥、真实 `.env`、许可证密钥和私人备份保存在仓库之外；`.gitignore` 不能替代提交前检查。第三方软件使用官方链接下载，并遵循各自的许可证。
