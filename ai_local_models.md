# AI Local Models

I use Ollama to install local ai models because for me it is the quickest way to access ai locally on any device any time. 

<br>

- download ollama on [ollama](https://www.ollama.com) or via terminal (Linux):
```
sudo apt install curl

curl -fsSL https://ollama.com/install.sh | sh
```

- pull a model:
```
ollama pull qwen3.5:2b
```

- chat with a model:
```
ollama run qwen3.5:2b
```

- stop a model after using it:
```
ollama stop qwen3.5:2b
```

- you can install [openwebui](https://openwebui.com/) to make it clearer to talk with a model.


# My Preferred Tiny AI Models

_05/26/2026_

This document outlines my personal preferences regarding the tiny AI models I utilize for various daily tasks.

## Model List

| Name                  | Size  | Notes |
|----------------------|-------|-------|
| qwen3.5:4b            | 3.4 GB | Best for hard, long, and precise tasks |
| qwen3.5:2b            | 2.7 GB | Light reasoning for precise tasks when i have time |
| gemma4:e2b            | 7.2 GB | Good when tasks vary a lot during a chat | 
| granite4.1:8b         | 5.3 GB | Big model when i have to make something that the 3b model cant handle |
| granite4.1:3b         | 2.1 GB | Fastest response time with very accurate and grounded responces |
| ministral-3:3b        | 3.0 GB | ? idk maybe i was testing it|
| gemma3:4b             | 3.3 GB | I have been using gemma3 until granite4.1 came out |

## Preferences and Rationale

### qwen3.5 Series
- Those are the best to help me coding and making stuff

### granite4.1 Series
- Absolute fastes models that respond quick and help me problem solving

## Conclusion

Choosing the right AI local model is crucial for optimizing performance at work.
