# Procedural Knowledge Graph extraction with Large Language Models
We introduce a prompt-based pipeline for extracting procedural knowledge graphs from text with LLMs.

This pipeline is able to:
- extract sequential steps from a procedure in natural language without any formatting or structure
- extract the tools needed to perform each steps
- extract the actions to be performed in each step
- generate a knowledge graph including all triples about the procedure, its steps, actions, and tools, according to an ontology given as reference

## Experimental setting
For our experiments, we:
- used the GPT-3.5 Turbo model (the [gpt-3.5-turbo-16k version](https://platform.openai.com/docs/models/gpt-3-5-turbo))
- set the temperature parameter to 0
- rely on the [LangChain framework](https://www.langchain.com/)

### Dataset
Procedures used in the prompt engineering refinement process, and in the evaluation, are selected from [WikiHow](https://wikihow.com/)

We reuse [this JSON dataset available on GitHub](https://github.com/zharry29/wikihow-goal-step)
