# Finetuning with PEFT

## Hugging Face API Key
To use the Hugging Face API, you need to set up your API key. You can do this by running the following command in your terminal:

```bash
huggingface-cli login
```
This will prompt you to enter your Hugging Face API key. You can find your API key in your Hugging Face account settings.
## PEFT
PEFT (Parameter-Efficient Fine-Tuning) is a method for fine-tuning large language models (LLMs) with a small number of trainable parameters. It allows you to adapt LLMs to specific tasks without the need for full model training, making it more efficient and cost-effective.
## LoRA
LoRA (Low-Rank Adaptation) is a specific PEFT method that introduces low-rank matrices into the model's architecture. This allows for efficient fine-tuning by only updating a small number of parameters while keeping the majority of the model's weights frozen.
## QLoRA
QLoRA (Quantized Low-Rank Adaptation) is an extension of LoRA that combines quantization techniques with low-rank adaptation. It further reduces the memory footprint and computational requirements during fine-tuning, making it suitable for resource-constrained environments.