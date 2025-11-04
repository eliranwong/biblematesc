### 设定虚拟环境

例如：

```
cd
python3 -m venv biblematesc
source biblematesc/bin/activate
pip install --upgrade pip biblematesc
export PATH=$PATH:$HOME/biblematesc/bin
echo "export PATH=$PATH:$HOME/biblematesc/bin" >> ~/.bashrc
biblematesc
```

### Vertex AI 整合支援

由于某些装置上可能存在相容性问题，因此 `google-genai` 函式库会作为单独的安装提供。

若要将 Vertex AI 与 BibleMate AI 搭配使用，请安装必要的函式库：

> pip install --upgrade "biblematesc[genai]"

### 升级

再次执行：

> pip install --upgrade biblematesc

### 开发者适用

> pip install -e .
