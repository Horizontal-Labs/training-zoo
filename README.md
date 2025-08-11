# training-zoo

A modular training repository for experimenting with Parameter-Efficient Fine-Tuning (PEFT) techniques on transformer models for argument mining tasks. Features implementations across encoder models (RoBERTa, DeBERTa, ModernBERT) and decoder models (TinyLlama, Mistral) using LoRA adapters. Not all training approaches lead to final PEFT adapters (only TinyLlama & ModernBERT).

## Quick Start

### Local Setup
```bash
# Clone repository
git clone https://github.com/Horizontal-Labs/training-zoo.git
cd training-zoo

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# Install dependencies
pip install -r requirements.txt
```

### Google Colab
Click the "Open in Colab" badges in the notebooks to run directly in your browser.

## 📁 Repository Structure

```
training-zoo/
├── decoder/             # Decoder model training (TinyLlama, Mistral)
├── encoder/             # Encoder model training (RoBERTa, DeBERTa, ModernBERT)
├── docs/                # Detailed documentation and guides
├── requirements.txt     # Python dependencies
└── README.md            # This file
```

## Experiments

### Encoder Models
- **Multi-task PEFT**: Shared encoder fine-tuned across multiple argument mining tasks
- **Task-specific heads**: Separate classification layers for different argument components
- **LoRA adaptation**: Parameter-efficient fine-tuning of language models
- **Models**: RoBERTa, DeBERTa, ModernBERT

### Decoder Models  
- **Instruction-based fine-tuning**: Natural language instructions for argument mining
- **LoRA adaptation**: Parameter-efficient fine-tuning of large language models
- **Models**: TinyLlama, Mistral

## Tasks

Our models are trained on four core argument mining tasks:

1. **ADU Identification**: Detecting argumentative discourse units
2. **ADU Classification**: Distinguishing claims from premises  
3. **Stance Classification**: Determining pro/con positions
4. **Relationship Identification**: Finding supportive/contradictory relationships

## Notebooks Overview
### Decoder
- Finetuning_PEFT_Decoder_Mistral.ipynb: PEFT finetuning with Mistral
- Finetuning_PEFT_Decoder_TinyLlama.ipynb: PEFT finetuning with TinyLlama
- Test-interference-finetuned-tinyLLAMA.ipynb: Inference testing

### Encoder
- Finetuning_PEFT_encoder-RoBERTa.ipynb
- Finetuning_PEFT_encoder-modernBERT.ipynb
- deberta_benchmark_eval_done.ipynb
  
## Fine Tuning Data

We used real-world argument mining datasets for fine tuning combining:
- **args.me**: 300K+ arguments from debate portals with stance annotations
- **IBM Debater®**: 2,394 manually annotated claims across 55 topics

The data was stored in a database, data preprocessing and schema details are documented in the [Argument Mining DB](https://github.com/Horizontal-Labs/argument-mining-db).

## Documentation

Comprehensive documentation is available in our [wiki](../../wiki):
- PEFT methodology and configurations
- Test Interference
- Local development setup guides

## Technical Stack

- **Frameworks**: PyTorch, Transformers, PEFT
- **Techniques**: LoRA, Multi-task Learning
- **Models**: ModernBERT, RoBERTa, DeBERTa, TinyLlama, Mistral
