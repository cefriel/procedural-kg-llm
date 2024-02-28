# Procedural Knowledge Graph extraction with Large Language Models
We introduce a **prompt-based pipeline** for extracting **procedural knowledge graphs** from text with LLMs.

This pipeline is able to:
- extract **sequential steps** from a procedure in natural language without any formatting or structure
- extract the **tools** needed to perform each steps
- extract the **actions** to be performed in each step
- generate a **knowledge graph** including all triples about the procedure, its steps, actions, and tools, according to an **ontology given as reference**

![PK-CoT-evaluation](https://github.com/cefriel/procedural-kg-llm/assets/36740200/870c9f0e-95d2-4b4a-ad2e-bd280c7e597c)


## Experimental setting
For our experiments, we:
- used the GPT-3.5 Turbo model (the [gpt-3.5-turbo-16k version](https://platform.openai.com/docs/models/gpt-3-5-turbo))
- set the temperature parameter to 0
- rely on the [LangChain framework](https://www.langchain.com/)

Procedures used in the prompt engineering refinement process, and in the evaluation, are selected from [WikiHow](https://wikihow.com/)

We reuse [this JSON dataset available on GitHub](https://github.com/zharry29/wikihow-goal-step)

## How to navigate this repository
### pk-kg-extraction
This folder contains:
- the notebook with the whole pipeline of 7 prompts, based on Chain-of-Thought prompting (the notebook also reports the actual pieces of text containing the procedures used as input)
- the notebooks xxx

The repository defines a `docker-compose.yml` file to run the Jupyter notebooks as containers via Docker. 
The containers can be run all at once or separately.

The notebooks can be executed running the container, from the folder with the .yml file, with the command:
```
docker-compose up --force-recreate
```

### data
- **json**: this folder contains the input procedures in the original json format
- **output-ttl**: this folder contains the output turtle KGs generated from the textual procedures
- **ontology**: this folder contains the demo procedural ontology used as reference in the experiments

### evaluation
This folder contains materials and results from the human assessment of the LLM results

