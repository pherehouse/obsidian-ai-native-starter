# Obsidian AI 原生起步包

这是一个帮助你快速配置 Obsidian AI 工作环境的起步包，也配套文章《别再把 AI 只当聊天框：用 Obsidian 搭一个 AI 原生工作空间》。

## 1. 先安装 Obsidian

- 官方下载：<https://obsidian.md/download>
- 国内镜像：<https://obsidian.bijitongbu.site/>

安装后，创建自己的第一个 Vault，并复制它的完整路径。

## 2. 安装配置包（二选一）

### 方式 A：下载 ZIP（不用 Git）

打开 GitHub 项目页面，点击 **Code → Download ZIP**，或直接下载：

<https://github.com/pherehouse/obsidian-ai-native-starter/archive/refs/heads/main.zip>

### 方式 B：使用 Git

如果已经安装 Git，也可以直接运行：

```bash
git clone https://github.com/pherehouse/obsidian-ai-native-starter.git
```

无论选择哪种方式，打开项目目录，把 `.obsidian/plugins/` 下的 `docxer`、`markitdown`、`terminal` 三个文件夹复制到自己的 `Vault/.obsidian/plugins/`。

只复制这三个插件文件夹，不要用整个 `.obsidian` 覆盖自己的仓库。复制后重启 Obsidian，在 **设置 → 社区插件** 中启用它们。

### 看不到 `.obsidian`？

- **macOS**：在 Finder 中按 `Command + Shift + .`；
- **Windows**：文件资源管理器选择 **查看 → 显示 → 隐藏的项目**。

## 3. 交给 AI 自动安装（可选）

如果希望让 AI 代为下载和复制，可以使用下面提示词；它与上面的两种手动安装方式任选其一。把提示词复制到 WorkBuddy、TraeWork、Codex 等支持本地文件操作的 AI 工具中，并填入自己的 Vault 路径。

```text
我的 Obsidian 仓库路径是：
【把 Vault 的完整路径粘贴到这里】

我没有 Git，请使用 HTTPS 下载并解压这个配置包：
https://github.com/pherehouse/obsidian-ai-native-starter/archive/refs/heads/main.zip

请按以下规则操作：
1. 先确认上面的路径确实是一个 Obsidian Vault；
2. 只把配置包 .obsidian/plugins/ 下的 docxer、markitdown、terminal 三个插件文件夹复制到我的 Vault/.obsidian/plugins/；
3. 不要覆盖 Vault 中其他插件、主题、快捷键或 workspace 配置；
4. 如果目标插件已经存在，先改名备份，再复制新版本；
5. 在 Vault 根目录新建“收件箱”“工作”“资料”“归档”四个文件夹；
6. 新建“收件箱/AI 原生起步.md”，说明插件已经复制完成，并提醒我重启 Obsidian 后到“设置 → 社区插件”启用插件；
7. 不要修改已有笔记；无法下载或无法写入时，直接告诉我具体原因，不要猜测成功。

全部完成后，只汇报实际创建和复制了哪些文件。
```

如果 AI 工具没有下载或写入本地文件的权限，就手动下载 ZIP 并复制插件。

## 4. 这三个插件分别做什么

| 插件 | 作用 | 版本 | 来源 |
| --- | --- | --- | --- |
| Docxer | 预览 Word，并转换为 Markdown | 2.3.1 | [obsidian-docxer](https://github.com/Developer-Mike/obsidian-docxer) |
| MarkItDown File Converter | 将 PDF、Word、PPT、Excel、网页等转成 Markdown | 2.1.0 | [obsidian-markitdown](https://github.com/ethanolivertroy/obsidian-markitdown) |
| Terminal | 在 Obsidian 内打开终端，运行 AI CLI | 3.25.0 | [obsidian-terminal](https://github.com/polyipseity/obsidian-terminal) |

MarkItDown 首次使用需要 Python 和 `markitdown` 包，按插件设置中的检查或安装提示操作。

## 5. 让 AI 更懂 Obsidian：安装 Skill

不必先学习 CLI 命令。WorkBuddy 和 TraeWork 都可以在技能中心搜索 **Obsidian**，直接安装相关技能。

也可以使用 GitHub 上的 [`obsidian-cli` Skill](https://github.com/kepano/obsidian-skills/tree/main/skills/obsidian-cli)。它负责教 AI 使用 Obsidian 的搜索、创建、双链和属性等能力。安装 Skill 后，按工具提示开启 Obsidian CLI 即可。

如果技能中心没有显示，直接把上面的 GitHub 地址导入即可。

## 6. 第一次体验：让 AI 生成一套北京旅行资料

插件装好后，把下面提示词复制到 AI 聊天窗口，并填入 Vault 路径：

```text
我的 Obsidian 仓库路径是：
【把仓库的完整路径粘贴到这里】

请在这个仓库中新建一个“北京三日游”项目。

背景：
有朋友第一次来北京，准备玩三天。
希望去故宫、八达岭长城和颐和园，也想体验北京本地美食。
行程不要太赶，尽量减少来回奔波。

请直接完成以下工作：
1. 新建“北京三日游”文件夹；
2. 建立“行程”“清单”“资料”三个子文件夹；
3. 生成三天的行程安排，每天单独保存为一篇 Markdown；
4. 生成景点预约、美食推荐和行前准备清单；
5. 创建一篇“旅行总览”，用 Obsidian 双链连接所有笔记；
6. 最后生成一份“北京旅行规划报告”。

要求：
- 所有文件使用中文名称和 Markdown 格式；
- 只在新建的“北京三日游”文件夹内操作；
- 不要修改仓库中已有的内容；
- 无法确认的票价、开放时间和预约政策，标记为“出发前核实”；
- 不要中途询问，全部完成后再告诉我生成了哪些内容。
```

## 版权说明

插件作者、源代码和许可协议归各自原作者所有，详见 [`NOTICE.md`](NOTICE.md)。本仓库只做配套整理，不修改插件代码。
