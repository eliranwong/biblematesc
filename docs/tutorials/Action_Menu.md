# 🏃 操作选单

| 命令 | 描述 |
|---|---|
| `.new` | 新对话 |
| `.exit` | 退出 BibleMate AI |
| `.backend` | 更改后端 |
| `.mode` | 更改 AI 模式 |
| `.tools` | 列出可用工具 |
| `.plans` | 列出可用计划 |
| `.resources` | 列出可用资源 |
| `.editprompt` | 编辑当前提示 |
| `.backup` | 备份对话 |
| `.reload` | 重新载入当前对话 |
| `.edit` | 编辑当前对话 |
| `.trim` | 修剪当前对话 |
| `.import` | 汇入对话 |
| `.export` | 汇出对话 |
| `.find` | 搜寻对话 |
| `.content` | 显示当前目录内容 |
| `.open` | 开启档案或目录 |
| `.ideas` | 产生想法 |
| `.autotool` | 切换自动工具选择 |
| `.autosuggest` | 切换自动输入建议 |
| `.autoprompt` | 切换自动提示工程 |
| `.light` | 切换轻量级上下文 |
| `.steps` | 设定最大步骤数 |
| `.matches` | 设定最大语意符合数 |
| `.download` | 下载资料档案 |
| `.help` | 显示说明页面 |

有些指令设计用于从 UniqueBible App 检索内容：

| 命令 | 描述 |
|---|---|
| `.bible` | 开启圣经经文 |
| `.chapter` | 开启圣经章节 |
| `.compare` | 比较圣经经文 |
| `.comparechapter` | 比较圣经章节 |
| `.chronology` | 开启圣经年代表 |
| `.commentary` | 开启注释 |
| `.aicommentary` | 开启 AI 注释 |
| `.index` | 开启经文研究索引 |
| `.translation` | 开启经文分析和翻译 |
| `.discourse` | 开启语篇分析 |
| `.morphology` | 开启形态学资料 |
| `.xref` | 开启串珠 |
| `.treasury` | 开启 TSKE |
| `.search` | 搜寻圣经 |
| `.parallel` | 搜寻圣经平行经文 |
| `.promise` | 搜寻圣经应许 |
| `.dictionary` | 搜寻辞典 |
| `.encyclopedia` | 搜寻百科全书 |
| `.lexicon` | 搜寻原文辞典 |
| `.topic` | 搜寻圣经主题 |
| `.name` | 搜寻圣经名称 |
| `.character` | 搜寻圣经人物 |
| `.locations` | 搜寻圣经地点 |

快捷键 `Ctrl+B`、`Ctrl+C`、`Ctrl+V` 和 `Ctrl+X` 设计用于在 BibleMate AI 中开启 UBA 内容 [[阅读](https://github.com/eliranwong/biblemate#%EF%B8%8F-keyboard-shortcuts)]。

## 备注：

* 输入 `.` 开启操作选单以选择操作。
* 使用 `.light` 启用或停用*轻量级上下文*。当*轻量级上下文*启用时（预设），BibleMate 执行速度稍快，工具回应品质略有牺牲。当*轻量级上下文*停用时，将使用完整上下文，这会消耗更多权杖进行处理，但提供更高的回应品质。
* 若要使用 `.import`，您需要指定一个包含已储存对话的 python 档案。每次执行备份时，对话都会储存到一个档案中。请检查讯息 `Conversation backup saved to ...` 或在 `~/agentmake/computemate` 中找到备份。除了仅载入对话，您还可以同时载入对话及其主要计划。为此，请指定一个包含 `conversation.py` 和 `master_plan.md` 的备份目录路径。
* 若要使用 `.open`，您需要指定要开启的档案或目录。
* `.edit` 指令可让您使用我们内建的文字编辑器编辑当前对话。您可以自订以使用您喜欢的文字编辑器。输入 `.backend` 并使用呼叫您喜欢的文字编辑器的指令变更 `DEFAULT_TEXT_EDITOR` 的值。
* 使用 `.autosuggest` 切换自动输入建议。如果停用，您可以使用 `TAB` 键开启输入建议选单。
* 使用 `.reload` 重新载入上次储存的对话（如果有的话）。这对于在对话因任何原因中断后继续未完成的代理流程很有用。
* 指令 `.matches` 仅适用于本机 MCP 连线。它不适用于远端 MCP 连线，因为本机设定的变更不会影响远端伺服器中的设定。
* 当 `.` 后面的内容与上面列出的操作指令不符时，请以 `.` 开头您的请求以直接检索圣经经文或章节，或执行圣经搜寻。例如：
    - 输入 `.John 3:16` 阅读约翰福音 3:16
    - 输入 `.John 3:16; Rm 5:8` 阅读约翰福音 3:16 和罗马书 5:8
    - 输入 `.John 3` 阅读约翰福音第 3 章
    - 输入 `.John 3, 4` 阅读约翰福音第 3 章和第 4 章
    - 输入 `.Jesus love` 执行 `耶稣 爱` 的圣经搜寻
