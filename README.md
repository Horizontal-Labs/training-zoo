# training-zoo

A modular training repository for experimenting with finetuning encoder and decoder models using PEFT techniques across various architectures like RoBERTa, DeBERTa, modernBERT, TinyLlama, and Mistral. Includes benchmarking, stance classification, and inference demos. Not all approaches lead to producive PEFT adapters!

The repository implements and evaluates multiple transformer-based approaches using different NLP model architectures:

### Encoder Models
- **Multi-Task Finetuning**  
  A shared encoder is fine-tuned across multiple tasks using separate classification heads for:
  - Argument Component Identification (claims, premises)
  - Relation Classification (e.g., pro, con)

### Decoder-Only Models
- **Prompting / In-Context Learning**  
  Uses zero-shot or few-shot prompts to guide large language models in recognizing argumentative structures.
- **Instruction-Based Multi-Task Finetuning**  
  Fine-tuning decoder models with task-specific natural language instructions.

## Folder Structure
```
training-zoo/
├── decoder/             # Training Notebooks + fine-tuned Decoder-only LoRa adapters (e.g. Mistral)
├── encoder/             # Training Notebooks + fine-tuned Encoder-only LoRa adapters (e.g. BERT, RoBERTa)
├── docs/                # Documentation ressources
├── requirements.txt     # Python dependencies
├── README.md            # Project overview and instructions
├── LICENSE              # Project license
```

## Data
The [Argument-Mining Repo](https://github.com/Horizontal-Labs/Argument-Mining) contains the datasets used for training and testing. 

## Notebooks Overview
### Decoder
- Finetuning_PEFT_Decoder_Mistral.ipynb: PEFT finetuning with Mistral
- Finetuning_PEFT_Decoder_TinyLlama.ipynb: PEFT finetuning with TinyLlama
- Test-interference-finetuned-tinyLLAMA.ipynb: Inference testing

### Encoder
- Finetuning_PEFT_encoder-RoBERTa.ipynb
- Finetuning_PEFT_encoder-modernBERT.ipynb
- deberta_benchmark_eval_done.ipynb

## Documentation
Further Documentation  lives in the docs/ folder:
- finetuning_peft.md: Overview of PEFT methods used
- run_colab_locally.md: How to run notebooks locally 
- data_base.md: Dataset explanations
- training_log.md: Training logs

## Getting started
### Run on Windows
This is a guide to setup the repo on a Windows machine

#### Clone repo
With access to [githubg.com/org/horizontal-labs/training-zoo](https://github.com/Horizontal-Labs/training-zoo) run the following command in your terminal:

```bash
git clone https://github.com/Horizontal-Labs/training-zoo.git
```

#### Initialize and update submodules
After cloning the repository, you need to initialize and update the submodules:

```bash
cd training-zoo
git submodule init
git submodule update
```

#### Create virtual environment
```bash
python -m venv venv
```

#### Activate virtual environment
```bash
venv\Scripts\activate
```
#### Install requirements
```bash
pip install -r requirements.txt
```

### Run in Colab
You can run the notebooks in Google Colab. To do this, open the notebook you want to run and click on the "Open in Colab" button at the top of the notebook. This will open the notebook in Google Colab, where you can run it without any additional setup.

Alrernatively, you can start clone a notebook from the repo and run it in Colab. To do this, open Google Colab and click on "File" > "Open notebook". In the dialog that appears, select the "GitHub" tab and select the URL of the notebook you want to clone. This will create a copy of the notebook in your Google Drive, where you can run it without any additional setup. Please save your progress as a commit to the repo.
