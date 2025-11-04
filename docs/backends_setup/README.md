# 🧠 支援的 AI 后端

由 AgentMake AI 驱动，BibleMate AI 让使用者可以灵活使用各种 AI 后端。更多资讯请参阅 https://github.com/eliranwong/agentmake#supported-backends

为了比较，我们在下面的测试中使用相同的主题「深入研究耶利米哀歌 3:22-24」测试了一些支援的后端：

BibleMate AI + `Azure + ChatGPT 5` https://youtu.be/QvPIyHOhrP0

BibleMate AI + `Gemini API + Gemini 2.5 Flash` https://youtu.be/AZ-zEl_StC0

BibleMate AI + `Mistral Large` https://youtu.be/7sBfj2TMoOE

BibleMate AI + `DeepSeek 3.1` https://youtu.be/FUr--ULDCZM

BibleMate AI + `Groq + GPT-OSS 120B` https://youtu.be/7sBfj2TMoOE

BibleMate AI + `Groq + Llama 3.3 70B` https://youtu.be/oKQyIEnMM8M

BibleMate AI + `XAI + Grok 4` https://youtu.be/JgcxciOc_Ys

## 后端设定范例

更多详细资讯请参阅 https://github.com/eliranwong/biblematesc/tree/main/docs/backends_setup。

## 提示

为了快速上手，我们建议从 `googleai` 后端开始，该后端已与 BibleMate AI 进行了广泛的测试。您可以免费获取 Gemini API 金钥。更多资讯，请浏览：[https://github.com/eliranwong/biblematesc/blob/main/docs/backends_setup/googleai.md](https://github.com/eliranwong/biblematesc/blob/main/docs/backends_setup/googleai.md)。

# ⚙️ 设定 AI 后端

启动 BibleMate AI 后，输入：

> .backend

将会开启一个文字编辑器，让您编辑 AgentMake AI 设定。将 `DEFAULT_AI_BACKEND` 变更为您选择的 AI 后端，并在适当的位置输入 API 金钥。

您可以使用 CLI 选项 `-b` 或 `--backend` 暂时覆写预设的 AI 后端。例如：

> biblematesc -b googleai

## 设定 UBA API [可选]

您可以选择性地透过编辑以下项目来设定 UBA API 后端：

```
# Tool: UBA API
UBA_API_LOCAL_PORT=8080
UBA_API_ENDPOINT="https://bible.gospelchurch.uk/plain"
UBA_API_TIMEOUT=10
UBA_API_PRIVATE_KEY=
```

## 设定远端 MCP 伺服器验证 [可选]

您可以选择性地透过编辑以下项目来设定远端 MCP 伺服器的验证资讯：

```
# BibleMate AI
BIBLEMATE_STATIC_TOKEN=
BIBLEMATE_MCP_PUBLIC_KEY=
BIBLEMATE_MCP_PRIVATE_KEY=
BIBLEMATE_MCP_ISSUER=
BIBLEMATE_MCP_AUDIENCE=
```

## 更多范例

请在 https://github.com/eliranwong/biblematesc/tree/main/docs/backends_setup 查看个别范例
