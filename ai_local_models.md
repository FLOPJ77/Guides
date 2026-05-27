# AI Local Models

I use Ollama to install local ai models because for me it is the quickest way to access ai locally on any device any time. 

<br>

- download ollama on [ollama.com](https://www.ollama.com) or via terminal (Linux):
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


<br>
<br>


# My Preferred Tiny AI Models

_05/26/2026_

This document outlines my personal preferences regarding the tiny AI models I utilize for various daily tasks.

<br>

## Model List

| Name                  | Size  | Notes |
|----------------------|-------|-------|
| granite4.1:3b         | 2.1 GB | Fastest response time with very accurate and grounded responces |
| granite4.1:8b         | 5.3 GB | Big model when i have to make something that the 3b model cant handle |
| qwen3.5:4b            | 3.4 GB | Best for hard, long, and precise tasks |
| qwen3.5:2b            | 2.7 GB | Light reasoning for precise tasks when i have time |
| gemma4:e2b            | 7.2 GB | Good when tasks vary a lot during a chat | 
| gemma3:4b             | 3.3 GB | I have been using gemma3 until granite4.1 came out |
| ministral-3:3b        | 3.0 GB | ? idk maybe i was testing it|

<br>

## Preferences
 
- granite4.1 Series: Absolute fastes models that respond quick and help me problem solving

- qwen3.5 Series: Those are the best to help me coding and making stuff


<br>
<br>


## Benchmark

I have done a quick performance benchmark using **Ollama**. I provided the same prompt to all models to measure generation speed and efficiency running on CPU.

**Prompt:**
> *Explain the concept of 'inertia' in two paragraphs.*

### Environment & Hardware
* **OS:** Ubuntu 24.04.4 LTS
* **Tool:** Ollama
* **CPU:** Intel® Core™ i7-1165G7 
* **RAM:** 40GB

<br>


*NON REASONING*
<img width="964" height="519" alt="NR-speed" src="https://github.com/user-attachments/assets/75f085cb-bd4d-451e-bfb5-b060d64804d1" />

*NON REASONING*
<img width="964" height="519" alt="NR-time" src="https://github.com/user-attachments/assets/8616f4d2-dc7c-4b63-b039-dd0b6f1426a4" />


*REASONING*
<img width="964" height="519" alt="R-speed" src="https://github.com/user-attachments/assets/b78ac73b-7973-49be-a2c9-6761d6dd9346" />

*REASONING*
<img width="964" height="519" alt="R-time" src="https://github.com/user-attachments/assets/c443e001-b407-47c5-93c1-deaa9b9f1f00" />


<br>

## Results 

- Non-Reasoning Models are optimized for fast, direct responses and daily terminal tasks.

- Reasoning Models have internal "Thinking" process for complex logic that add precision but with a trade off, the waiting time.



<br>

## Conclusion

Choosing the right AI local model is crucial for optimizing performance at work and i prefer Granite4.1:3b for most of the tasks i do.






