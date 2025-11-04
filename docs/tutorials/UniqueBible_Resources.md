# ✝️ UniqueBible 资源

我们在 BibleMate AI 中汇集了两者的优点，以增强您的圣经学习。除了动态 AI 工具，我们还透过 BibleMate AI 提示整合了对大多数 [UniqueBible 资源](https://github.com/eliranwong/UniqueBible) 的直接存取。在与 AI 代理的对话中，您可以随时将 UniqueBible App 资料直接纳入讨论，以丰富学习流程和内容。

在 BibleMate AI 提示中输入 `.resources` 以查看可用资源。可用 UniqueBible 资源的数量取决于您在后端设定中配置的 [UniqueBible 网路伺服器](https://github.com/eliranwong/UniqueBible)。预设情况下，BibleMate AI 使用运行在 https://bible.gospelchurch.uk 的 UniqueBible 网路伺服器。UniqueBible 伺服器高度可自订；您可以设定一个带有自订资源的本地伺服器以与 BibleMate AI 一起使用。

要将 BibleMate AI 与您的本地伺服器连接，请在 BibleMate AI 提示中输入 `.backend`，找到下面的会话，并填写您的本地伺服器详细资讯：

```
# 工具：UBA API
UBA_API_LOCAL_PORT=8080
UBA_API_ENDPOINT="http://127.0.0.1:8080/plain"
UBA_API_TIMEOUT=10
UBA_API_PRIVATE_KEY=
```

提示：以 `//` 开头您的提示，以从输入建议中查看可用资源。

# 键盘快捷键

UniqueBible App 的大多数资源都可以透过热键存取：

`Ctrl+B` 开启圣经选项 [助记符：B -> Bible]
<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/2016b4cc-f370-4aa1-bcd9-8b8b30f8a727" />

`Ctrl+C` 开启圣经注释功能 [助记符：C -> Commentary]
<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/9a175b0e-7385-4aaa-9f6e-00f57ae675fa" />

`Ctrl+V` 开启单节经文学习功能 [助记符：V -> Verse]
<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/2089542c-573d-47f7-ae57-4704295b9417" />

`Ctrl+X` 开启串珠功能 [助记符：X -> Cross-references]
<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/aa2e31fb-e89c-4af8-bd5e-53e631fc12ce" />

`Ctrl+F` 搜寻圣经资料库 [助记符：F -> Find]。此功能需要额外设定，请参阅 https://github.com/eliranwong/biblematesc/blob/main/docs/installation/macOS.md#%E6%94%AF%E6%8F%B4%E8%AA%9E%E7%BE%A9%E6%90%9C%E7%B4%A2-semantic-searches-optional
<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/a5005066-029f-432f-88a2-771dddd52f8f" />
