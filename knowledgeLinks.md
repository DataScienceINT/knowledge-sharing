# Centralisation of resources 

**Please add links in the corresponding section or a new section if you find something interesting.**

These can be papers, blog posts, podcasts, models, videos, courses, books, etc. Demos developed within the HU (ex: markdown files demonstrating a packages) should also be included.
If possible, please include a short description/key takeaway(s).

## Science

- [The Palindrome](https://thepalindrome.substack.com/) Stories about how mathematics impact science and technology.
- [Intro to modern statistics](https://openintro-ims.netlify.app/)
- [Consensus.app](https://consensus.app/search/) lets you ask a question and the app finds papers that answer yes or no to this question.
- [Connected papers](https://www.connectedpapers.com/) Finds papers that are similar to each other and presents them in a graph. (these papers can site each other but don't have too)


## General Data Science / Machine Learning

- [The Gradient](https://thegradient.pub/). Digital magazine about trends in AI/machine learning, founded by Stanford Artificial Intelligence Laboratory. A lot of essay-style articles (a few are linked below). 
- [Discovering novel algorithms with AlphaTensor](https://www.deepmind.com/blog/discovering-novel-algorithms-with-alphatensor). Discovery of novel algorithms by AI. Broad possibilities for application in data science/computer science in general. Link to the GitHub repo and article in the article.
- [Illustrated Machine Learning](https://illustrated-machine-learning.github.io/) A website illustrating a variety of ML concepts, a bit "back of the envelop" drawing style.
- [New machine setup](https://github.com/RamiKrispin/awesome-ds-setting). Tutorial on how to set up a new machine for Data Science. Based on MacOS.
- [Equality of odds](https://mlu-explain.github.io/equality-of-odds/). One technique to prevent bias in ML.
- [Bruno Rodrigues blog](https://www.brodrigues.co/blog/). Nice technical blog, more on the software engineering side. Posts include a 4-parter on Nix for reproducible science.
- [Telling stories with data](https://tellingstorieswithdata.com/). Haven't read it all, but seems like a nice book/reference for data analysis, reproducibility and communication.
- [ML papers explained](https://github.com/dair-ai/ML-Papers-Explained). Links to a collection of Medium posts to explain ML papers/concepts, e.g. Transformers and all the LLM zoo, CNNs, vision models, etc.
- [Four kinds of optimization](https://tratt.net/laurie/blog/2023/four_kinds_of_optimisation.html). A short dive into how to optimize the running time of your programs. Explores trade-offs of 4 solutions: use a better algorithm, a better data structure, a lower-level programming language (e.g. rewrite some Python in Rust) or accept a less precise solution.

## Natural Language Processing

- [Creating knowledge graphs from unstructured text](https://faircookbook.elixir-europe.org/content/recipes/interoperability/creating-knowledge-graph-from-unstructured-text.html). FAIR cookbook recipe with all steps (and tools) from literature to knowledge graph.
- [Prodigy Open AI recipes](https://github.com/explosion/prodigy-openai-recipes). Recipes to obtain high quality dataset from LLM and small annotation effort.
- [Understanding LLM: A reading list](https://sebastianraschka.com/blog/2023/llm-reading-list.html). Reading list of founding papers for Transformers-based language models.
- [LLM applications for production](https://huyenchip.com/2023/04/11/llm-engineering.html). Very interesting post with tips for prompt engineering, evaluation and optimization, model finetuning, and best practices for LLM use in general.
- [Impact of LLMs on scientific discovery](https://arxiv.org/pdf/2311.07361.pdf). A Microsoft Research paper investigating the performance of GPT-4 for various scientific tasks (drug discovery, materials design, molecular simulations, etc.). 230 pages...
- [Tackling hallucinations ion LLMs](https://magazine.sebastianraschka.com/p/research-papers-in-november-2023). A blog post with multiple links to research papers detailing how to deal with (and reduce) LLMs generating factually wrong information.
- [The Pipe](https://github.com/emcf/thepipe): Python package that does markdown extraction from a variety of formats, including PDFs and Word.


### RAG
- [paperQA](https://github.com/whitead/paper-qa/). Minimal package to do QA on PDFs.
- [LlamaIndex](https://docs.llamaindex.ai/en/stable/). Data framework for LLM applications.
- [LlamaParse](https://www.llamaindex.ai/blog/launching-the-first-genai-native-document-parsing-platform). Connected to previous link - with json parsing capabilities for tables, text (and images?).
- [Tips & Tricks for RAG](https://www.youtube.com/watch?app=desktop&v=ZP1F9z-S7T0&feature=youtu.be). From LlamaIndex, YouTube video for putting RAG in production.
- [Real time RAG chatbot](https://blog.streamlit.io/build-a-real-time-rag-chatbot-google-drive-sharepoint/). Blogpost on building RAG with "real time" updates of the knowledge base.
- [Production RAG](https://docs.google.com/presentation/d/1bPv3lrayGe4LOn2v_Go_n7o5xDrGvmfLAQ83Q0EI8GY/edit#slide=id.p). Presentation on choices to make while building a RAG (also on evaluation, deployment, budget).
- [Embeddings quantization](https://huggingface.co/blog/embedding-quantization). Cost and latency reductions thanks to embeddings quantization.
- [Retrieval Augmented fine tuning](https://www.youtube.com/watch?app=desktop&v=sqPckknlgDc). Approach to fine tune LLMs to retrieve relevant documents.
- [Rerankers](https://www.answer.ai/posts/2024-09-16-rerankers.html): Low-dependency python package to unify interface to most common rerankers models.

### Models

- [SAPBERT](https://huggingface.co/cambridgeltl/SapBERT-from-PubMedBERT-fulltext). HuggingFace model for biomedical entities representation.
- [PubMedBERT](https://huggingface.co/microsoft/BiomedNLP-PubMedBERT-base-uncased-abstract)
- [REBEL](https://github.com/Babelscape/rebel). Relationship extraction model. HuggingFace model, pluggable on spaCy. Ranked 3rd on relationship extraction the Adverse Drug Events dataset.
- [BioGPT](https://github.com/microsoft/BioGPT). Pre-trained on biomedical literature, claims to outperform SoT models on most biomedical NLP tasks.
- [Efficient Transformers](https://developers.reinfer.io/blog/2022/04/11/efficient-transformers-part2). How to make LLM more efficient. Covers knowledge distillation and fine-tuning.
- [PKPDAI](https://github.com/PKPDAI). Suite of models specialized for PK modeling. Document classifier and NER.

### Corpora

- [EuropePMC](https://www.biorxiv.org/content/10.1101/2023.02.20.529292v1.full.pdf+html). Annotated full text corpus for gene/proteins, diseases and organisms. Link is to the BioarXiv paper, with details on how to access and reuse the resource.

### Papers/Books

- [Natural Language Processing with Transformers](https://github.com/nlp-with-transformers/notebooks)

### Interesting articles

- [Designing a GPT-3 for science](https://future.com/how-to-build-gpt-3-for-science). Key TAs: death to PDF format! Articles are a substrate for information combination.
- [Lessons from the GPT-4chan controversy](https://thegradient.pub/gpt-4chan-lessons/). Article about ethics in AI. Interesting TA: possibility to "gate" potentially harmful models so that they are only accessible to researchers.

### Talks
- [NLP Summit](https://www.nlpsummit.org/) A collection of talks about NLP, particularly focused on biomedical/healthcare. Look into tab "Watch past summits".

## Graph ML

## Bayesian

- [Statistical Rethinking](https://github.com/rmcelreath/stat_rethinking_2023) Course developed by Richard McElreath focused on (bayesian) modeling. Given live once a year, the link contains the most recent (2023) material.

## Neural networks

- [Understanding LSTMs](https://medium.com/@mumbaiyachori/understanding-lstms-6d50b10f2a37)
-[What are embeddings?](https://vickiboykis.com/what_are_embeddings/) A deep (82 pages!) dive into embeddings and what they are on a conceptual, mathematical and engineering level.

## Software/Packages/Tools

### Technical tutorials

- [Installing PyTorch Geometric on Mac M1 with Accelerated GPU Support](https://medium.com/@jgbrasier/installing-pytorch-geometric-on-mac-m1-with-accelerated-gpu-support-2e7118535c50). Building an environment for graph machine learning on Macbook with M1.
- [Setting Python Development Environment with VScode and Docker](https://github.com/RamiKrispin/vscode-python?#readme). 

### Productivity tools
- [Foam](https://foambubble.github.io/foam/). Knowledge management and sharing tool.
- [Explainpaper](https://www.explainpaper.com/). Upload a paper, highlight confusing terms and get an explanation returned (provided by with GPT-3 model).

### Python packages
- [Polars](https://github.com/pola-rs/polars/tree/master/py-polars). New library claimed to be much faster than Pandas for dataframes in Python.
- [FAISS](https://faiss.ai/) A library for efficient similarity search between vectors. Written in C++ but Python wrappers.
- [SafeTensors](https://github.com/huggingface/safetensors). New (as of June 2023) default in HuggingFace to save/load models, as it has improved security (vs Pickle).
- [Guardrails AI](https://docs.getguardrails.ai/). Python package to verify structure  and quality of LLM outputs. Can be useful to check for bias or type errors, but not a resource to verify facts.

### R packages
- [RPolars](https://rpolars.github.io/articles/rpolars.html). The above library now also for R. Again, claims to be much faster than all tidverse tool, but I find the grammar of it quite repulsive TBH.
- [WebR](https://www.tidyverse.org/blog/2023/03/webr-0-1-0/). R package to run R code directly in browser from a website.
- [Rang](http://blog.schochastics.net/post/rang-make-ancient-r-code-run-again/) R package to help reproducibility of old code in R.
- [messydates](https://globalgov.github.io/messydates/). A package to make date formats tidy.


## Miscellaneous
For interesting information that is not necessarily DS-related. Mostly dataviz TBH.

- [Bioicons](https://bioicons.com/) A free library of science icons and logos (SVG), that goes beyond your standard PPT icons.
- [Designing color keys](https://blog.datawrapper.de/color-keys-for-data-visualizations/). Blogpost explaining how to create easy-to-read color keys (=legends) for your charts).
- [Friends don't let friends](https://github.com/cxli233/FriendsDontLetFriends). An opinionated guide on common mistakes in the use of (scientific) graphs.

