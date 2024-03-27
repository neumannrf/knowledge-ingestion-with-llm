# knowledge-ingestion-with-llm

Jupyter notebooks using [IBM Generative AI Python SDK](https://github.com/IBM/ibm-generative-ai) to extract material information from literature.

## Installation

The only pre-requisites are `python3` and `pipenv`. Open this folder in a command-line terminal and
run the commands below.

```Shell
pipenv install
pipenv run jupyter-lab ibm_genai.ipynb
```

The Jupyter notebook should open automatically as a browser window.

## Authentication

Create an `.env` file in this folder with the following content.

```Shell
GENAI_KEY=<your-api-key>
GENAI_API=https://bam-api.res.ibm.com
```

You can copy your API key from the panel on the right at the <https://bam.res.ibm.com/> page.

## Usage

In the `use-cases/` folders, you can find three JSON files:

* `instruction.json`: containing the instructions to the large language models.
* `training_examples.json`: list of objects containing `input` and `output` fields for the prompt.
* `test_examples.json`: list of objects containing `input` and `output` fields for validating the result.

Both example JSON files, for test and training, have the same format:

* `input` is a string with the paragraph to be processed, and
* `output` is a string with the Python dictionary extracted from the paragraph.
