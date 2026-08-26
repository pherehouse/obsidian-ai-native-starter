# Obsidian AI 原生起步包

这是配套文章《别再把 AI 只当聊天框：用 Obsidian 搭一个 AI 原生工作空间》的可直接复制配置包。

它只包含文章中真正需要复制的 3 个社区插件：

- **Docxer**：预览 Word，并把 `.docx` 转成 Markdown；
- **MarkItDown File Converter**：把 PDF、Word、PPT、Excel、网页等资料转成 Markdown；
- **Terminal**：在 Obsidian 内打开终端，运行 AI CLI。

文章里提到的 **Obsidian CLI** 不是一个社区插件，而是 Obsidian 提供的 CLI 能力。它需要在你的 Obsidian 版本中单独开启；无论你从 WorkBuddy、TraeWork 等外部 AI 进入，还是从 Obsidian 内部运行 AI CLI，都可以调用它。

## Obsidian 安装包

如果还没有安装 Obsidian，可以直接下载本项目 Release 中的 1.13.7 安装包：

- [macOS 安装包（DMG）](https://github.com/pherehouse/obsidian-ai-native-starter/releases/download/obsidian-1.13.7/Obsidian-1.13.7.dmg)
- [Windows 安装包（EXE）](https://github.com/pherehouse/obsidian-ai-native-starter/releases/download/obsidian-1.13.7/Obsidian-1.13.7.exe)

两个安装包都比较大，GitHub 普通仓库单个文件不能超过 100 MB，所以它们作为 Release 附件提供，不放在代码目录里。也可以从 [Obsidian 官网](https://obsidian.md/download) 下载最新版。

安装包的版本和校验值记录在 [`安装包与下载.md`](安装包与下载.md)。

## 不用 Git：下载 ZIP 安装

1. 打开本仓库的 GitHub 页面，点击 **Code → Download ZIP**，或直接下载：

   `https://github.com/pherehouse/obsidian-ai-native-starter/archive/refs/heads/main.zip`

2. 解压 ZIP。
3. 找到你自己的 Obsidian 仓库（Vault）文件夹。
4. 把解压目录中的 `.obsidian/plugins/` 下这 3 个文件夹复制到你的仓库 `.obsidian/plugins/` 下：

   ```text
   docxer/
   markitdown/
   terminal/
   ```

   只复制这 3 个插件文件夹，不要用整个 `.obsidian` 文件夹覆盖自己的仓库配置。

5. 重启 Obsidian，进入 **设置 → 社区插件**，开启这 3 个插件。
6. MarkItDown 首次使用时需要 Python。打开插件设置，按提示检查或安装 `markitdown` Python 包。

### 看不到 `.obsidian`？

`.obsidian` 是隐藏文件夹，需要先显示隐藏文件：

- **macOS**：在 Finder 中按 `Command + Shift + .`；
- **Windows**：打开文件资源管理器，选择 **查看 → 显示 → 隐藏的项目**（旧版 Windows 选择 **查看 → 隐藏的项目**）。

## 复制给 WorkBuddy / TraeWork 的快速安装提示词

把下面整段复制到 WorkBuddy、TraeWork、Codex 或其他可以操作本地文件的 AI 工具中。把第一行的仓库路径替换成自己的路径。

```text
我的 Obsidian 仓库路径是：
【把 Vault 的完整路径粘贴到这里】

我没有 Git，请使用 HTTPS 下载并解压这个配置包：
https://github.com/pherehouse/obsidian-ai-native-starter/archive/refs/heads/main.zip

如果电脑还没有 Obsidian，请先按系统下载并安装：
- macOS：https://github.com/pherehouse/obsidian-ai-native-starter/releases/download/obsidian-1.13.7/Obsidian-1.13.7.dmg
- Windows：https://github.com/pherehouse/obsidian-ai-native-starter/releases/download/obsidian-1.13.7/Obsidian-1.13.7.exe

请按以下规则操作：
1. 先确认上面的路径确实是一个 Obsidian Vault；
2. 只把配置包 .obsidian/plugins/ 下的 docxer、markitdown、terminal 三个插件文件夹复制到我的 Vault/.obsidian/plugins/；
3. 不要覆盖 Vault 中其他插件、主题、快捷键或 workspace 配置；
4. 如果目标插件已经存在，先在 Vault/.obsidian/plugins/ 下改名备份，再复制新版本；
5. 在 Vault 根目录新建“收件箱”“工作”“资料”“归档”四个文件夹；
6. 新建“收件箱/AI 原生起步.md”，说明插件已经复制完成，并提醒我重启 Obsidian 后到“设置 → 社区插件”启用插件；
7. 不要修改已有笔记；无法下载或无法写入时，直接告诉我具体原因，不要猜测成功。

全部完成后，只汇报实际创建和复制了哪些文件。
```

如果 AI 工具没有下载或写入本地文件的权限，就按上面的“下载 ZIP 安装”方式手动复制；提示词本身不需要 Git。

## 第一次体验：让 AI 生成一套北京旅行资料

插件装好后，先不要搭复杂知识库。复制 [`提示词/北京三日游-首次体验.md`](提示词/北京三日游-首次体验.md) 到 AI 聊天窗口，把 Vault 路径填进去，就能看到 AI 如何直接在本地生成 Markdown 文件。

## 手动安装

- [macOS 手动安装](手动安装/macOS.md)
- [Windows 手动安装](手动安装/Windows.md)

## 插件与来源

插件版本、作者和来源见 [`插件清单.md`](插件清单.md)。本仓库只做个人使用便利的文件整理，不改变插件代码；插件著作权和许可归原作者所有。
