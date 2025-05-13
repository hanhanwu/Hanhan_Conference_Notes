# AI Agent Conference 2025

## Tips from AI Practicioners
### Input
* Create & use "best practice" examples as the input
* Can use synthetic data to generate the high quality of data input

### Evaluation
* Can use multiple LLM models in auto eval to reduce bias
* Let business experts to break the tool for evaluation

### Key Components
* Data context matters
* Evaluation is the key
  * build feedback loops is important
  * can use query rewriting to deal with ambiguity
  * monitoring is needed
 
### Synthetic Data Generation for RAG Chatbot and Text-to-SQL
* [ON THE DIVERSITY OF SYNTHETIC DATA AND ITS IMPACT ON TRAINING LARGE LANGUAGE MODELS][2]
  * This work underscores the importance of <b>not just the quantity and quality, but also the diversity</b> of synthetic data in enhancing LLM capabilities. 
  * The authors use multiple pre-trained LLMs to generate synthetic training data. These LLMs interact with each other in structured dialogues or collaborative tasks (e.g., one posing a question, another answering, etc.).
  * The generation process is prompt-driven, and the prompts are varied systematically to introduce diversity: Different instructions, styles, topics, and formats. Some prompts encourage reasoning, others focus on factual recall, storytelling, or coding.
  * After generating samples, the authors cluster the synthetic data using a semantic embedding model. They then select samples from diverse clusters to maximize diversity in the final dataset.
    * Choose an embedding model to encode text into semantically meaningful vectors.
    * Run clustering on the embeddings
    * Evaluate clustering quality
    * Select representative samples from each cluster to maximize diversity
   
* [Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone][3]
  * This paper uses carefully filtered public data and synthetic data as input
  * Using larger, more capable LLMs can generate: Instructions, Responses, Explanations, Reasoning chains, Dialogues, Math & logic, etc.

 
### Research Papers from JP Morgan
* [GENERATING STRUCTURED PLAN REPRESENTATION OF PROCEDURES WITH LLMS][1]
  * SOPStruct presents a transformative approach to SOPs (Standard Operating Procedures) management by leveraging LLMs to generate structured, decision-tree-based representations of procedures. This method addresses the limitations of traditional process modeling techniques, offering enhanced clarity, standardization, and automation potential. By facilitating better comprehension and execution of SOPs, SOPStruct paves the way for future advancements in automated procedure optimization.
 
### Timescale's Idea Building SQL Agent
* Semantic Catalog Search
  * 3 corpuses of structured knowledge
    * schema desctiptions: tables, columns, views, etc.
    * stand-alone facts: business logic, data semantics
    * example queries: user questions & SQL
  * Encode each corpus separately via vector embeddings
  * Enables semantic search on catelog for relevant context  
  * RAG designed around text-to-SQL
    * Retrieve example questions --> SQL
    * Retrieve business facts
    * Retrieve object descriptions and corresponding references
  * <b>Iteratively Refining Missing Context</b>
    * If LLM requests more info, for each new keyword or phase, iteratively search semantic catelog for examples, objects, facts
  * Returns {question, context}
* SQL Validation
  * Pass candidate SQL to PSQL Explain 
    * validate SQL syntax
    * validate object references (tables, columns, etc.)
    * estimate costs
    * cannot hallucinate - inexpensively planned against actual database
* 🤔 Hmm, when the user query is quite unpredictable, using RAG here seems too expensive to me. The validation idea has some inspiration

[1]:https://arxiv.org/pdf/2504.00029v1
[2]:https://arxiv.org/pdf/2410.15226v2
[3]:https://arxiv.org/pdf/2404.14219v4
