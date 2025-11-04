# ✒️ 内建文字编辑器

<img width="866" height="629" alt="Image" src="https://github.com/user-attachments/assets/d62658d0-10df-4e56-8de3-58787600327f" />

您可以透过在 BibleMate AI 提示栏位中输入 `.editprompt` 或按下 `Ctrl+O` 来使用我们的内建文字编辑器编辑当前提示。

您也可以单独执行 `etextedit` 来启动内建编辑器。

您可以在我们的内建文字编辑器 `etextedit` 中使用以 BibleMate AI 和 AgentMake AI 建构的外挂程式。

BibleMate AI 随附安装了外挂程式 `Extract Bible References` 和 `Insert Bible Text`。

您也可以新增自己的 `etextedit` 外挂程式并将它们放置在 `~/etextedit/plugins` 中。

阅读更多关于 `etextedit` 的资讯：https://github.com/eliranwong/etextedit

# 汇出为 DOCX 或 PDF [选用]

`etextedit` 提供将内容汇出为 DOCX 和 PDF 档案的选项。

- 汇出内容为 DOCX 格式需要 `pandoc`。例如，在 Debian/Ubuntu 上安装：

> sudo apt install pandoc

- 汇出内容为 PDF 格式需要 `pdflatex`。例如，在 Debian/Ubuntu 上安装：

> sudo apt install texlive-full

# 第三方文字编辑器 [选用]

您可以使用自己选择的第三方文字编辑器。在 BibleMate AI 提示中输入 `.backend` 并将 `DEFAULT_TEXT_EDITOR` 的值指定为呼叫您喜欢的文字编辑器的命令，例如 `micro -softwrap true -wordwrap true`。若要使用内建文字编辑器 `etextedit` 进行更改，您只需一个步骤，即储存 `Ctrl+S` 或退出 `Ctrl+Q`，即可返回 BibleMate AI 提示。然而，对于第三方文字编辑器，您需要在退出前先储存更改。
