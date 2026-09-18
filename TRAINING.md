# Luminas Astra 7 — Training

This document describes the training process used to develop **Luminas Astra 7**.

## Base Model

Astra 7 was developed from:

**Qwen2.5-Coder-7B-Instruct**

The model was adapted using parameter-efficient fine-tuning rather than training all model parameters from scratch.

## Fine-Tuning Method

Astra 7 was trained using **QLoRA**, allowing the model to be fine-tuned in 4-bit precision while keeping GPU memory requirements relatively low.

### Configuration

| Setting               | Value           |
| --------------------- | --------------- |
| Fine-tuning method    | QLoRA           |
| Quantization          | 4-bit           |
| Framework             | Unsloth         |
| GPU                   | NVIDIA Tesla T4 |
| Dataset               | ~33K examples   |
| Epochs                | 1               |
| Batch size            | 1               |
| Gradient accumulation | 4               |
| Trainable parameters  | ~1.05%          |
| Context length        | 32K             |

## Dataset

The training dataset contained approximately **33,000 software-engineering examples** covering areas such as:

* Programming
* Debugging
* Software engineering
* Technical problem solving
* Development workflows
* Agent-oriented tasks

The dataset was prepared and validated before training to ensure compatibility with the model's conversational format.

## Training Process

The overall pipeline was:

```text
Base Model
     ↓
Dataset Preparation
     ↓
Dataset Validation
     ↓
4-bit Model Loading
     ↓
QLoRA Fine-Tuning
     ↓
Checkpoint Validation
     ↓
Adapter Merge
     ↓
GGUF Conversion
     ↓
Local Inference Validation
     ↓
Luminas Astra 7
```

## Training Run

The final training run completed approximately **8,264 optimization steps**.

The recorded training loss at the end of the run was approximately:

```text
Training Loss: 0.00438
```

Training was performed on an NVIDIA Tesla T4 environment using Unsloth.

## Post-Training

After fine-tuning, the trained adapter was merged with the base model and converted into **GGUF** format for local inference.

The resulting model was tested locally before release.

## Release

The final GGUF model is distributed through the Luminas AI Hugging Face repository:

https://huggingface.co/luminas-ai/Luminas-Astra-7

The GitHub repository contains the engineering and documentation surrounding the model rather than the large model weights themselves.

---

**Luminas AI**
Building autonomous AI software engineers.
