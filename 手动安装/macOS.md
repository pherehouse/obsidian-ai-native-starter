# macOS 手动安装

## 1. 下载并解压

打开 GitHub 项目页面，选择 **Code → Download ZIP**，或使用：

<https://github.com/pherehouse/obsidian-ai-native-starter/archive/refs/heads/main.zip>

双击 ZIP 解压。

## 2. 显示隐藏文件

在 Finder 中打开解压后的项目目录和你的 Vault，按 `Command + Shift + .` 显示 `.obsidian`。

## 3. 复制插件

打开解压目录：

```text
obsidian-ai-native-starter/.obsidian/plugins/
```

把 `docxer`、`markitdown`、`terminal` 三个文件夹复制到：

```text
你的 Vault/.obsidian/plugins/
```

不要用整个 `.obsidian` 文件夹覆盖 Vault。若已有同名插件，先把旧文件夹改名为 `插件名.backup`。

## 4. 启用插件

重启 Obsidian，打开 **设置 → 社区插件**，启用三个插件。MarkItDown 首次使用时，按插件设置提示检查 Python 和 `markitdown` 包。

也可以在终端中复制单个插件（请替换路径）：

```bash
cp -R "/你的下载目录/obsidian-ai-native-starter/.obsidian/plugins/docxer" "/你的Vault/.obsidian/plugins/"
cp -R "/你的下载目录/obsidian-ai-native-starter/.obsidian/plugins/markitdown" "/你的Vault/.obsidian/plugins/"
cp -R "/你的下载目录/obsidian-ai-native-starter/.obsidian/plugins/terminal" "/你的Vault/.obsidian/plugins/"
```
