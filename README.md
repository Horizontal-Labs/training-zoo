# training-zoo

This repository is the home for all the fine-tuning and training Jupyter Notebooks in an argument mining project that nvestigates how modern NLP techniques—particularly transformer-based language models—can be used to build robust **Argument Mining Pipelines**. It explores various transformer architectures and learning approaches to recognize, classify and relate argumentative content.

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
├── decoder/             # Training Notebooks + fine-tuned Decoder-only models (e.g. Mistral)
├── encoder/             # Training Notebooks + fine-tuned Encoder-only models (e.g. BERT, RoBERTa)
├── docs/                # Documentation ressources
├── requirements.txt     # Python dependencies
├── README.md            # Project overview and instructions
├── LICENSE              # Project license
```

## Data
The [Argument-Mining Repo](https://github.com/Horizontal-Labs/Argument-Mining) contains the datasets used for training and testing. 

## Getting started
### Run on Windows
This is a guide to setup the repo on a Windows machine

#### Clone repo
With access to [githubg.com/org/horizontal-labs/training-zoo](https://github.com/Horizontal-Labs/training-zoo) run the following command in your terminal:

```bash
git clone https://github.com/Horizontal-Labs/training-zoo.git
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
