# Luminas Astra 7

**Luminas Astra 7** is a 7B-class AI software engineering model developed by **Luminas AI**, designed for practical coding, debugging, technical problem-solving, and autonomous software engineering workflows.

Astra 7 is built on **Qwen2.5-Coder-7B-Instruct** and fine-tuned using **QLoRA** with a curated software-engineering dataset.

## Overview

|                    |                               |
| ------------------ | ----------------------------- |
| **Model**          | Luminas Astra 7               |
| **Parameters**     | ~7.6B                         |
| **Base Model**     | Qwen2.5-Coder-7B-Instruct     |
| **Training**       | QLoRA / 4-bit                 |
| **Context Length** | 32K                           |
| **Primary Focus**  | Software Engineering & Coding |
| **Model Format**   | GGUF                          |
| **Developer**      | Luminas AI                    |

## Capabilities

Astra 7 is optimized for:

* Software engineering
* Code generation and modification
* Debugging and error analysis
* Technical reasoning
* Terminal and development workflows
* Multi-step problem solving
* Agent-oriented software tasks

## Development

Astra 7 was fine-tuned using **Unsloth** with a QLoRA training setup designed to make 7B-class model development possible on consumer/cloud GPUs with limited VRAM.

The final model was converted to **GGUF** and validated for local inference.

For more information about the training process and configuration, see [`TRAINING.md`](TRAINING.md).

## Model

The model weights are hosted separately on Hugging Face.

**Hugging Face:**
https://huggingface.co/luminas-ai/Luminas-Astra-7

## Local Usage

Astra 7 can be run locally using compatible GGUF inference runtimes such as **llama.cpp** and **Ollama**.

Example with Ollama:

```bash
ollama run Luminas-Astra-7
```

## Project Status

**Released — Astra 7**

Astra 7 is the first released model in the Luminas AI model family.

Future development will focus on improving coding ability, reasoning, agentic workflows, and overall reliability.

---

### Luminas AI

**Luminas AI — Building autonomous AI software engineers.**
