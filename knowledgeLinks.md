# Centralisation of resources 

**Please add links in the corresponding section or a new section if you find something interesting.**

These can be papers, blog posts, podcasts, models, videos, courses, books, etc. Demos developed within the HU (ex: markdown files demonstrating a packages) should also be included.
If possible, please include a short description/key takeaway(s).

## Science

- [The Palindrome](https://thepalindrome.substack.com/) Stories about how mathematics impact science and technology.
- [Intro to modern statistics](https://openintro-ims.netlify.app/)


## General Data Science / Machine Learning

- [The Gradient](https://thegradient.pub/). Digital magazine about trends in AI/machine learning, founded by Stanford Artificial Intelligence Laboratory. A lot of essay-style articles (a few are linked below). 
- [Discovering novel algorithms with AlphaTensor](https://www.deepmind.com/blog/discovering-novel-algorithms-with-alphatensor). Discovery of novel algorithms by AI. Broad possibilities for application in data science/computer science in general. Link to the GitHub repo and article in the article.
- [Illustrated Machine Learning](https://illustrated-machine-learning.github.io/) A website illustrating a variety of ML concepts, a bit "back of the envelop" drawing style.
- [New machine setup](https://github.com/RamiKrispin/awesome-ds-setting). Tutorial on how to set up a new machine for Data Science. Based on MacOS.
- [Equality of odds](https://mlu-explain.github.io/equality-of-odds/). One technique to prevent bias in ML.


## Natural Language Processing

- [Creating knowledge graphs from unstructured text](https://faircookbook.elixir-europe.org/content/recipes/interoperability/creating-knowledge-graph-from-unstructured-text.html). FAIR cookbook recipe with all steps (and tools) from literature to knowledge graph.
- [Prodigy Open AI recipes](https://github.com/explosion/prodigy-openai-recipes). Recipes to obtain high quality dataset from LLM and small annotation effort.
- [Understanding LLM: A reading list](https://sebastianraschka.com/blog/2023/llm-reading-list.html). Reading list of founding papers for Transformers-based language models.
- [LLM applications for production](https://huyenchip.com/2023/04/11/llm-engineering.html). Very interesting post with tips for prompt engineering, evaluation and optimization, model finetuning, and best practices for LLM use in general.

### Models

- [SAPBERT](https://huggingface.co/cambridgeltl/SapBERT-from-PubMedBERT-fulltext). HuggingFace model for biomedical entities representation.
- [PubMedBERT](https://huggingface.co/microsoft/BiomedNLP-PubMedBERT-base-uncased-abstract)
- [REBEL](https://github.com/Babelscape/rebel). Relationship extraction model. HuggingFace model, pluggable on spaCy. Ranked 3rd on relationship extraction the Adverse Drug Events dataset.
- [BioGPT](https://github.com/microsoft/BioGPT). Pre-trained on biomedical literature, claims to outperform SoT models on most biomedical NLP tasks.
- [Efficient Transformers](https://developers.reinfer.io/blog/2022/04/11/efficient-transformers-part2). How to make LLM more efficient. Covers knowledge distillation and fine-tuning.

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

## Software/Packages/Tools

### Technical tutorial

- [Installing PyTorch Geometric on Mac M1 with Accelerated GPU Support](https://medium.com/@jgbrasier/installing-pytorch-geometric-on-mac-m1-with-accelerated-gpu-support-2e7118535c50). Building an environment for graph machine learning on Macbook with M1.

### Productivity tools
- [Foam](https://foambubble.github.io/foam/). Knowledge management and sharing tool.
- [Explainpaper](https://www.explainpaper.com/). Upload a paper, highlight confusing terms and get an explanation returned (provided by with GPT-3 model).

### Python packages
- [Polars](https://github.com/pola-rs/polars/tree/master/py-polars). New library claimed to be much faster than Pandas for dataframes in Python.
- [FAISS](https://faiss.ai/) A library for efficient similarity search between vectors. What ToxTrack uses. Written in C++ but Python wrappers.

### R packages
- [RPolars](https://rpolars.github.io/articles/rpolars.html). The above library now also for R. Again, claims to be much faster than all tidverse tool, but I find the grammar of it quite repulsive TBH.
- [WebR](https://www.tidyverse.org/blog/2023/03/webr-0-1-0/). R package to run R code directly in browser from a website.
- [Rang](http://blog.schochastics.net/post/rang-make-ancient-r-code-run-again/) R package to help reproducibility of old code in R.


## Miscellaneous
For interesting information that is not necessarily DS-related.

- [Bioicons](https://bioicons.com/) A free library of science icons and logos (SVG), that goes beyond your standard PPT icons.

