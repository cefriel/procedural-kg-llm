# Procedural Knowledge Graph extraction  from Text with Large Language Models
We propose a **prompt-based pipeline** for extracting **procedural knowledge graphs** from text with LLMs.

This pipeline extracts **steps**, **actions**, **objects**, **equipment** and **temporal information** from a textual procedure, in order to populate a **Procedural KG** according to a **pre-defined ontology**.


<img width="449" alt="image" src="https://github.com/user-attachments/assets/9e5ffc9b-b692-4a95-92a2-7de21682b838">



## Experimental setting
For our experiments, we:
- used the [GPT 4o model](https://platform.openai.com/docs/models/gpt-4o)
- set the temperature parameter to 0
- rely on the [LangChain framework](https://www.langchain.com/)

Procedures used in the prompt engineering refinement process, and in the evaluation, are selected from [WikiHow](https://wikihow.com/)

We reuse [this JSON dataset available on GitHub](https://github.com/zharry29/wikihow-goal-step)

## How to navigate this repository
### pkg-extraction / notebooks
This folder contains:
- **pkg-extraction.ipynb**, the notebook with the pipeline of 2 prompts
- a subfolder **preliminary-experiments** containing the notebooks with our preliminary experiments

The repository defines a `docker-compose.yml` file to run the Jupyter notebooks as containers via Docker. 
The containers can be run all at once or separately.

The notebooks can be executed running the container, from the folder with the .yml file, with the command:
```
docker-compose up --force-recreate
```

A `credentials.json` file should be provided in the main folder with a valid key for the OpenAI API.

```
{
    "OPENAI_API_KEY": "PUT_HERE_YOUR_KEY"
}
```

### data-results
- **ontology**: this folder contains the procedural ontology used as reference in the experiments
- **clean-flat-panel-monitor**, **fix-rubbing-door**, **cook-honey-glazed-parsnips**, **plant-bare-root-tree**: these folders contain input and output data for the 4 procedures
- **preliminary-experiments**: this folder contains the results of previous experiments during the prompt engineering refinement process

### human-assessment
This folder contains:
- materials and results from the human assessment of the LLM results
- a subfolder **preliminary-experiments** containing the materials and results from the human assessment of our preliminary experiments

