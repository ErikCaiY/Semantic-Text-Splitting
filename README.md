# SEMANTIC CHUNKER

Using large language models (Moonshot) for semantic segmentation and summarization of PDF content.

使用大模型(Moonshot)对pdf内容进行语义切分与总结。

## DEMO

### quick start

#### config.json:
api_key: YOUR MOONSHOT API KEY

    https://platform.moonshot.cn/console/api-keys

source_dir: Your pdf dir

save_path: The dir save your results,

log_file: log

model_name: "moonshot-v1-128k",

temperature: 0.01,

max_token: 100000,

#### Run
```bash
pip install openai
pip install langchain-community
```

See ./chunkerExample.py

```bash
python ./chunkerExample
```

### Examples
You can find some examples in ./res
```
./res/1 计算机科学与技术专业.txt
./res/3 软件工程专业 (嵌入式系统).txt
./res/attentionIsAllYouNeed.txt
```

## Processing pdf in other language or using other LLM

If you want to process in other language, please modify the language of prompt (see ./semanticChunker/PROMPT.py ) or consider using alternative LLMs (like GPT-4o).

## todo list
1. [ ] Support for other LLMs.
   1.  [ ] ollama
   2.  [ ] openai
2. [ ] Sopport files in other formats.
   1. [ ] docx 
   2. [ ] txt
   3. [ ] markdown
