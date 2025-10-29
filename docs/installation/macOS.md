# 在 macOS 上安装 MateMate AI 中文版

BibleMate AI 支援 十多个 AI 供应端，如 OpenAI, Google Gemini, xAI, Groq ... 等。这页介绍其中一个方法，既免费又可以在一般的电脑配备上安装。

BibleMate AI 支援在 Windows 11, macOS, linux, ChromeOS, Android 上运作，基本的步骤离不开下面三个：

1. [登记 AI 供应云端服务](https://github.com/eliranwong/biblematesc/blob/main/docs/installation/macOS.md#%E7%AC%AC%E4%B8%80%E6%AD%A5---%E7%94%B3%E8%AB%8B-google-gemini-api-keys%E5%85%8D%E8%B2%BB)（如果有好的电脑配备，可以免去这步）
2. [安装 Python 3.8-3.12](https://github.com/eliranwong/biblematesc/blob/main/docs/installation/macOS.md#%E7%AC%AC%E4%BA%8C%E6%AD%A5---%E5%AE%89%E8%A3%9D-python)（Linux 系统一般都预设安装了 python，或可免这步）
3. [安装 BibleMate AI](https://github.com/eliranwong/biblematesc/blob/main/docs/installation/macOS.md#%E7%AC%AC%E4%B8%89%E6%AD%A5---%E5%AE%89%E8%A3%9D-biblemate-ai-%E4%B8%AD%E6%96%87%E7%89%88)

## 第一步 - 申请 Google Gemini API Keys（免费）

1. 开启网站 https://aistudio.google.com ，然后选择 `Get Started` ，并使用你个人的 Google Account 登入<img width="1281" height="461" alt="Image" src="https://github.com/user-attachments/assets/e9a54d02-c245-4331-9de2-0764e94bc561" />

2.  于左边目录选择 `Get API Key`，然后在右上角选择 `Create API Key`

<img width="1617" height="1056" alt="Image" src="https://github.com/user-attachments/assets/63d5f1ab-9ba1-4eee-a213-af58ccf73541" />

3. 先选择 `Create Project`，例如输入：BibleMate

<img width="512" height="329" alt="Image" src="https://github.com/user-attachments/assets/97d677d5-22c5-42b2-b9e7-f7106efcb09c" />

4. 输入 API 名称方便日后识别，例如输入：BibleMate

<img width="511" height="283" alt="Image" src="https://github.com/user-attachments/assets/9ceb7476-c56c-4459-90bd-69c4b168fceb" />

5. 复制 Copy 新建立的 API Key，并按你个人方式储存好，在第三步有用，在不要与其他人分享这个 API Key。

<img width="1043" height="263" alt="Image" src="https://github.com/user-attachments/assets/6373d1ce-f4f6-4529-899a-3d535a513f4a" />

备注：

* 可以不用理会 Billing，因为 Google 提供免费 Free Tier 使用。
* Free Tier 多用时会有 rate limit 限制，建议如果一家几口一起使用，多用几个不同成员的 Google Accounts 分别申请多几个 API Keys。
* 如想切换 Google Gemini 到其他 AI 供应端，可参考 https://github.com/eliranwong/biblematesc/tree/main/docs/backends_setup

## 第二步 - 安装 python 

1. 开启 [https://python.org](https://python.org) ，选择 `Downloads` -> `macOS`，切勿直接下载 3.14 版本，BibleMate AI 目前只支援 python versions 3.9-3.12
<img width="1503" height="660" alt="Image" src="https://github.com/user-attachments/assets/81f0eb85-20ea-4480-8ff5-17c0d4dac0e6" />

2. 选择 Download [macOS 64-bit universal2 installer](https://www.python.org/ftp/python/3.12.10/python-3.12.10-macos11.pkg) 。你也可以选用其他版本，但必须是在 3.9-3.12 这范围内。

<img width="987" height="865" alt="Image" src="https://github.com/user-attachments/assets/b3c7bcbb-da7e-4590-8d74-cce13a269605" />

3. 下载后，在你个人电脑的 Downloads 文件夹里找出新下载档案，然后双击开启，按指示安装

<img width="732" height="556" alt="Image" src="https://github.com/user-attachments/assets/7bed2aea-a381-4fa3-b7b9-c1582b88e3e3" />

## 第三步 - 安装 BibleMate AI 中文版

1. 开启 `Terminal` app （`Applications` -> `Utilities` -> `Terminal`）

<img width="1032" height="576" alt="Image" src="https://github.com/user-attachments/assets/126afe61-758e-404d-9e9f-8dccd6e9936d" />

2. 开启后，复制 Copy 下面七行指令，在 Terminal app 贴上 Paste，按 `Enter` 键执行

```
cd
python3 -m venv biblematesc
source biblematesc/bin/activate
pip install --upgrade pip "biblematesc[genai]"
echo "alias bmsc='$HOME/biblematesc/bin/bmsc'" >> .zprofile
echo "alias biblemate tc='$HOME/biblematesc/bin/biblematesc'" >> .zprofile
bmsc
```

3. 允许 Terminal app 连接网络

<img width="372" height="360" alt="Image" src="https://github.com/user-attachments/assets/667f10d0-075c-478b-a2f5-717b7decd936" />

4. 输入在第一步申请的 Google Gemini API Key。如果不想一个个字打进去，可以把 API Key 先复制 Copy，`然后按 Command+V` 贴上 Paste 这里（请用你有效的 API Key 取代 xxxxxxxxxxx）：

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/ee882eae-514f-4406-95cf-a40d1fe632ac" />

5. BibleMate AI 支援轮流使用数个 API Keys（用英文逗号 `,` 隔开多个 API Keys，但不要加空格）：

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/6520bcbf-ee7d-4727-8c1d-2fb36b7e3a69" />

6. 按下 `OK` 确定后，需要重新启动，在 Terminal App 上输入 `biblematesc` 或者 `bmsc` 即可。

<img width="890" height="124" alt="Image" src="https://github.com/user-attachments/assets/92332717-0011-4504-8bbc-f0b38721e63f" />

## 备注

* 所有 API Keys 只会储存在你的个人电脑上，储存的档案是 `~/agentmake/agentmake.env`。
* Terminal app，预设是白底黑字，预设的字体也很小。个人建议改用黑底白字，和增加字体大小。可以在 Terminal app 的 Settings 更改。

# 使用方法

1. 在 Terminal app 输入 `biblematesc` 或者 `bmsc` 即可进入 BibleMate AI 中文版。
2. 输入你的要求，然后按 `Ctrl+S` 确定，让 BibleMate AI 执行你的要求。

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/a2f84f01-e2e4-496e-9359-b8afd5dcc583" />

## 切换不同 AI 模式

BibleMate AI 支援三种 AI 模式 - 代理，搭档，对话 - 供使用者按需要随时切换：

* `代理`模式 - 全自动模式，AI 执行所有步骤
* `搭档`模式 - 半自动操作模式，使用者参与检阅及修改
* `对话`模式 - 简单一问一答的对话模式

1. 输入 `.mode` 开启 AI 模式选单：

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/47ecf9ed-fe07-4773-91f6-1cd9a8598d41" />

2. 选择其中一个模式

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/13a07479-1fd9-4cac-b379-c2c16a71525b" />

3. 切换后，输入你的要求，然后按 `Ctrl+S` 来确定

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/1514558a-5d8e-472e-b06f-2fb72ebb96dd" />

## 支援语义搜索 Semantic Searches [Optional]

你可以通过 BibleMate AI 搜索多项圣经资料，如圣经，原文字典，百科全书，圣经应许 ... 等，但需要两个额外的设置：

1. 在你的电脑上安装 Ollama （BibleMate AI 使用 Ollama 建立向量资料库） ，下载可参考 https://ollama.com/download
2. 在 BibleMate AI 输入要求 `.download`，按指示下载附加的资料库。

<img width="866" height="629" alt="Image" src="https://github.com/user-attachments/assets/1e8aa6b2-4c47-4fe0-9e9d-7d5163f88ea4" />

## 在不使用 AI 功能下，直接提取圣经和相关资源

BibleMate AI 预设连接[英伦福音教会](ttps://bible.gospelchurch.uk)的圣经网站 https://bible.gospelchurch.uk/traditional.html ，使用者可以随时直接提取有关圣经的研读资料，而不需要通过 AI 功能。

BibleMate AI 大多的功能都能通过快速键开启，其中五个组合正是为了快速开启圣经相关资料而设计的：

`Ctrl+B` 开启圣经选项 [帮助记忆：B -> Bible]

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/2016b4cc-f370-4aa1-bcd9-8b8b30f8a727" />

`Ctrl+C` 开启圣经注释功能 [帮助记忆：C -> Commentary]

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/9a175b0e-7385-4aaa-9f6e-00f57ae675fa" />

`Ctrl+V` 开启单节查考功能 [帮助记忆：V -> Verse]

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/2089542c-573d-47f7-ae57-4704295b9417" />

`Ctrl+X` 开启经文串珠功能 [帮助记忆：X -> Cross-references]

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/aa2e31fb-e89c-4af8-bd5e-53e631fc12ce" />

`Ctrl+F` 搜索圣经资料库 [帮助记忆：F -> Find] ，这项目需要额外设置，请参考 https://github.com/eliranwong/biblematesc/blob/main/docs/installation/macOS.md#%E6%94%AF%E6%8F%B4%E8%AA%9E%E7%BE%A9%E6%90%9C%E7%B4%A2-semantic-searches-optional

<img width="1002" height="697" alt="Image" src="https://github.com/user-attachments/assets/a5005066-029f-432f-88a2-771dddd52f8f" />

## 更多快速键

`Ctrl+Y` 开启帮助咨询

## 更多功能介绍

中文： https://github.com/eliranwong/biblematesc

英文： https://github.com/eliranwong/biblemate