# training-zoo

This repository is the home for all the fine-tuning and training Jupyter Notebooks.

Please add all requiered libraries as a `!pip install $required library` to your notebooks.

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