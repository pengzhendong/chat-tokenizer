# chat-tokenizer

## Usage

```python
from chat_tokenizer import ChatTokenizer
from transformers import AutoTokenizer


tokenizer = ChatTokenizer(AutoTokenizer.from_pretrained("qwen/Qwen2.5-0.5B-Instruct"))

audio_lens = [[4, 2], 3]
labels = [["今天天气不错", "哈哈"], "你好啊"]
label_ids, input_ids, label_lens, input_lens = tokenizer.batch_tokenize(audio_lens, labels)
input_ids = tokenizer.fill_labels(label_ids, input_ids)
```
