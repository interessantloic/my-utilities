# Syntax Highlight

## 解决什么问题

为 Finder 提供 Quick Look 扩展：选中文件并按空格，即可预览 YAML、源码和部分无扩展名文本的内容，支持语法高亮。

- 官方项目：<https://github.com/sbarex/SourceCodeSyntaxHighlight>
- 官方下载：<https://github.com/sbarex/SourceCodeSyntaxHighlight/releases>
- Homebrew 包名：`syntax-highlight`

## 安装与启用

```bash
brew install --cask syntax-highlight
open -a "Syntax Highlight"
```

必须至少打开应用一次，让 macOS 发现扩展。然后在较新的 macOS 中进入 **系统设置 → 通用 → 登录项与扩展 → 快速查看（Quick Look）**，点击信息按钮并开启 Syntax Highlight。不同系统版本的入口可能不同，可在系统设置中搜索 Quick Look。

关闭已有预览窗口，重新选择 `.yaml` 文件并按空格。可用以下无敏感内容的 YAML 验证：

```yaml
name: quick-look-test
enabled: true
```

## 文件类型说明

YAML 属于支持的格式；`.env` 这种仅以一个点开头的文件名，可能按无扩展名文本处理。实际预览还取决于系统识别到的文件类型（UTI）及其他已安装应用的类型关联。

`key.pub` 的支持情况尚未在新电脑上确认，需要单独测试。不要假设所有看起来像文本的文件都能自动交给同一个扩展。

## 安装后仍然只有图标

1. 确认已经打开过主应用。
2. 确认系统设置中的 Quick Look 扩展已开启。
3. 关闭预览窗口再试；仍无效时重启 Mac 后重试。
4. 用本机已下载的、包含内容的 YAML 文件测试，排除文件未下载的情况。
5. 以下只读命令可辅助检查扩展注册和具体文件类型：

   ```bash
   pluginkit -m -A -D | grep -i sbarex
   mdls -name kMDItemContentType -name kMDItemContentTypeTree "/path/to/example.yaml"
   ```

第二条命令中的路径需要替换为实际文件路径。扩展没有输出与文件类型不匹配是不同问题，应结合系统设置和具体文件继续排查。

## 配置迁移

基本预览功能只需安装并启用扩展。若希望恢复字体或配色，可在新电脑应用中重新设置。已有偏好文件通常位于 `~/Library/Preferences/org.sbarex.SourceCodeSyntaxHighlight.plist`；自定义主题与样式位于 `~/Library/Application Support/Syntax Highlight/`。这些属于可选的个人备份，不随此仓库发布。

## 参考

- [官方安装与扩展启用说明](https://github.com/sbarex/SourceCodeSyntaxHighlight#installation)
- [官方无扩展名文件说明](https://github.com/sbarex/SourceCodeSyntaxHighlight#plain-files)
- [Apple：登录项与扩展设置](https://support.apple.com/zh-cn/guide/mac-help/mtusr003/mac)
