## Prompt 1

```
You are an expert in information extraction, with a special background in procedures.

Consider the following procedure:
""
{example}
""

Q: generate sentences that include the verb/phrasal verb/idiomatic expression expressing the action (one sentence can have multiple actions, as you see fit), the direct object, that is the noun or pronoun being acted upon by the verb of the action (if any), the equipment that is any object needed for performing the action (if any), except for the direct objects of the action, time relevant for performing the action (if any)
If relevant for performing the action, include also implicit equipment that is not mentioned in the text.
A:
{example-extraction}


Consider the following process:
""
{procedure-for-llm}
""
Q: generate sentences that include the verb/phrasal verb/idiomatic expression expressing the action (one sentence can have multiple actions, as you see fit), the direct object, that is the noun or pronoun being acted upon by the verb of the action (if any), the equipment that is any object needed for performing the action (if any), except for the direct objects of the action, time relevant for performing the action (if any) 
If relevant for performing the action, include also implicit equipment that is not mentioned in the text.
A:
```

## Prompt 2

```
You are an expert in knowledge graph construction, with a special background in ontologies on procedural knowledge.


Consider this text:
""
{example-extraction}
""

Q: generate the RDF knowledge graph in Turtle format from it. You include exclusively the entities you're given in this text and only the entities you're given in this text. Do not include entities from other texts. Do not include text other than the RDF triples.
A:
{example-rdf}


Consider this text:
""
{llm-extraction}
""
Q: generate the RDF knowledge graph in Turtle format from it. You include exclusively the entities you're given in this text and only the entities you're given in this text. Do not include entities from other texts. Do not include text other than the RDF triples.
A:
```