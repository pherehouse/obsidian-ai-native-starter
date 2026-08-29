# Obsidian AI 原生起步包

这是《别再把 AI 只当聊天框：用 Obsidian 搭一个 AI 原生工作空间》的配套起步包，用来快速配置 Obsidian AI 工作环境。

## 1. 先安装 Obsidian

- 官方下载：<https://obsidian.md/download>
- 国内镜像：<https://obsidian.bijitongbu.site/>

安装后创建第一个 Vault。如果要让 AI 自动安装插件，再复制它的完整路径。

## 2. 安装配置包（二选一）

### 方式 A：下载 ZIP（不用 Git）

打开 GitHub 项目页面，点击 **Code → Download ZIP**，或直接下载：

<https://github.com/pherehouse/obsidian-ai-native-starter/archive/refs/heads/main.zip>

### 方式 B：使用 Git

如果已经安装 Git，也可以直接运行：

```bash
git clone https://github.com/pherehouse/obsidian-ai-native-starter.git
```

无论选择哪种方式，打开项目目录，把 `.obsidian/plugins/` 下的 `docxer`、`markitdown`、`md2html`、`obsidian-html-plugin`、`ppt-viewer`、`terminal`、`univer` 七个文件夹复制到自己的 `Vault/.obsidian/plugins/`。

只复制这些插件文件夹，不要用整个 `.obsidian` 覆盖自己的仓库。复制后重启 Obsidian，在 **设置 → 社区插件** 中启用它们。

如果无法访问插件市场，可以从作者的 [Smart Composer 1.2.9 官方发布页](https://github.com/glowingjade/obsidian-smart-composer/releases/tag/1.2.9) 手动安装。下载 `main.js`、`manifest.json`、`styles.css`，放入 `Vault/.obsidian/plugins/smart-composer/`。

### 看不到 `.obsidian`？

- **macOS**：在 Finder 中按 `Command + Shift + .`；
- **Windows**：文件资源管理器选择 **查看 → 显示 → 隐藏的项目**。

## 3. 交给 AI 自动安装（可选）

不想手动复制插件，也可以把下面的提示词交给 WorkBuddy、TraeWork、Codex 等支持本地文件操作的 AI，并填入 Vault 路径。

```text
我的 Obsidian 仓库路径是：
【把 Vault 的完整路径粘贴到这里】

我没有 Git，请使用 HTTPS 下载并解压这个配置包：
https://github.com/pherehouse/obsidian-ai-native-starter/archive/refs/heads/main.zip

请按以下规则操作：
1. 先确认上面的路径确实是一个 Obsidian Vault；
2. 只把配置包 .obsidian/plugins/ 下的 docxer、markitdown、md2html、obsidian-html-plugin、ppt-viewer、terminal、univer 七个插件文件夹复制到我的 Vault/.obsidian/plugins/；
3. 创建 Vault/.obsidian/plugins/smart-composer/，从 Smart Composer 作者的 1.2.9 官方发布页下载 main.js、manifest.json、styles.css 放入该文件夹：https://github.com/glowingjade/obsidian-smart-composer/releases/tag/1.2.9；
4. 不要覆盖 Vault 中其他插件、主题、快捷键或 workspace 配置；
5. 如果目标插件已经存在，先备份到 Vault 根目录的 .plugin-backups/，再复制新版本；不要把备份留在 .obsidian/plugins/ 内；
6. 不要修改已有笔记；无法下载或无法写入时，直接告诉我具体原因，不要猜测成功。

全部完成后，只汇报实际创建和复制了哪些文件。
```

如果 AI 工具没有下载或写入本地文件的权限，就手动下载 ZIP 并复制插件。

## 4. 插件说明

| 类别 | 插件 | 作用 | 版本 | 来源 |
| --- | --- | --- | --- | --- |
| 常见办公文档预览 + AI 处理 | Docxer | 预览 Word，并转换为 Markdown | 2.3.1 | [obsidian-docxer](https://github.com/Developer-Mike/obsidian-docxer) |
| 常见办公文档预览 | PPT Viewer | 直接预览 PPT、PPTX | 1.0.0 | phere |
| 常见办公文档预览 | Univer | 预览和编辑 Excel 等表格文件 | 1.1.5 | [obsidian-univer](https://github.com/dream-num/obsidian-univer) |
| AI 友好文档预览、处理与传播 | HTML Reader | 直接预览 HTML、HTM | 1.0.14 | 基于 [obsidian-html-plugin](https://github.com/nuthrash/obsidian-html-plugin)，由 phere 调整 |
| AI 友好文档预览、处理与传播 | MarkItDown File Converter | 将 PDF、Word、PPT、Excel、网页等转成 Markdown | 2.1.0 | [obsidian-markitdown](https://github.com/ethanolivertroy/obsidian-markitdown) |
| AI 友好文档预览、处理与传播 | md2html | 将 Markdown 转为带目录和样式的 HTML，方便浏览器阅读和分享 | 0.1.0 | phere |
| 单独安装 | Smart Composer | 与 AI 对话、引用 Vault 内容并协助编辑笔记 | 1.2.9 | [obsidian-smart-composer](https://github.com/glowingjade/obsidian-smart-composer) |
| 在 Obsidian 中使用 AI | Terminal | 在 Obsidian 内运行 AI CLI | 3.25.0 | [obsidian-terminal](https://github.com/polyipseity/obsidian-terminal) |

PPT Viewer、md2html 由 phere 编写；HTML Reader 基于原项目调整；其他插件版权归原作者所有。

MarkItDown 首次使用需要 Python 和 `markitdown` 包，按插件设置中的检查或安装提示操作。

Smart Composer 需要配置自己的模型服务；例如在 **设置 → Smart Composer → Providers** 中选择 DeepSeek，填入自己申请的 API Key，再选择模型即可。本配置包不包含任何账号或密钥。

## 5. 让 AI 更懂 Obsidian：安装 Skill

WorkBuddy 和 TraeWork 可以在技能中心搜索 **Obsidian**，安装相关技能。也可以按所用 AI 工具的说明，从 GitHub 安装 [`obsidian-cli` Skill](https://github.com/kepano/obsidian-skills/tree/main/skills/obsidian-cli)。安装后，按提示开启 Obsidian CLI。

## 6. 下一步

安装完成后，回到配套文章，复制“北京三日游”提示词完成第一次体验。

## 版权说明

插件作者、来源和改编情况详见 [`NOTICE.md`](NOTICE.md)。本仓库同时包含 phere 编写或调整的插件，以及其他原作者发布的第三方插件。
