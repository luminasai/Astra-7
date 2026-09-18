# Luminas Astra 7 — Model Card

## Model Details

**Model name:** Luminas Astra 7
**Developer:** Luminas AI
**Model family:** Luminas Astra
**Version:** 7
**Parameter count:** ~7.6B
**Base model:** Qwen2.5-Coder-7B-Instruct
**Model format:** GGUF
**Context length:** 32,768 tokens

## Description

Luminas Astra 7 is a fine-tuned AI model developed by Luminas AI with a focus on software engineering and practical technical problem-solving.

The model was developed to improve performance on coding, debugging, development workflows, and multi-step software engineering tasks while remaining suitable for local inference.

Astra 7 is based on Qwen2.5-Coder-7B-Instruct and was adapted using parameter-efficient fine-tuning.

## Training

### Method

* **Fine-tuning:** QLoRA
* **Quantization:** 4-bit
* **Framework:** Unsloth
* **Training hardware:** NVIDIA Tesla T4
* **Training examples:** ~33K
* **Epochs:** 1
* **Gradient accumulation:** 4
* **Batch size:** 1
* **Trainable parameters:** ~1.05%

The training process included dataset preparation, validation, fine-tuning, checkpoint validation, adapter merging, GGUF conversion, and local inference testing.

## Intended Use

Astra 7 is intended for:

* Code generation
* Code explanation
* Debugging
* Software development assistance
* Technical problem solving
* Development and terminal workflows
* Agent-oriented software engineering tasks

## Limitations

Astra 7 is a relatively small model and may produce incorrect, incomplete, or outdated information.

It should not be assumed to execute, verify, or test generated code unless connected to an appropriate execution environment.

Model performance can also vary depending on the prompt, context, inference settings, and runtime.

## Base Model & Attribution

Astra 7 is derived from **Qwen2.5-Coder-7B-Instruct**.

The original base model and its applicable license and attribution requirements remain relevant to this derivative model.

For the complete model and associated metadata, visit the Hugging Face repository:

https://huggingface.co/luminas-ai/Luminas-Astra-7

## Status

**Released**

Luminas Astra 7 is an experimental release from Luminas AI and serves as a foundation for future Luminas model development.
