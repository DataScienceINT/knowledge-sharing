# PyData Amsterdam 2024
These are the notes of the PyData conference in Amsterdam from 18-20th September, 2024.

## Tutorials

### LLM Agents - Ana Chaloska, Maria Bader

This was nice, some nice base code using LangChain - haven't tried the one using OpenAI API.
Workshop leaders were from industry and mentioned they prefer using OpenAI API for production as it is more stable than LangChain.
-[Repo](https://github.com/mkmbader/pydata_workshop_September2024)

### Prompt Hacking - Sander van Dorsten, Myrthe Lammerse

Really fun interactive workshop, where we engineered prompts to try and get a password from a chatbot.
- [Slides](https://amsterdam2024.pydata.org/cfp/talk/DTTGNH/)
- [Website - try it yourself](https://tensortrust.ai/)

### Web scraping - Fabien Vauchelles

Advanced web scraping techniques, including overcoming anti-bot measures (legally), etc.
Wasn't really fond of this one, lots of dependencies and not very clear explanations. If you are interested, here is the [repo](https://github.com/fabienvauchelles/scraping-workshop).

## Data flow with Prefect - Andy Hill

Didn't actually attend that one, but the material could be interesting.

- [repo](https://github.com/Cadarn/PyData-Prefect-Workshop)

## Sweet Summer Child Score - Laura Summers

No one metric that can apply to everything to evaluate fairness.
Library still needs to be revisited for LLMs (created in 2018) - though mostly applicable.
- [Material](https://summerscope.github.io/slides/summerchild-workshop/)
- [Another link to a practical ethics course](https://ethics.fast.ai/)
A cool workshop on identifying risk, ranking them, getting possible mitigation for them.

## Talks

### Open-source Multimodal AI in the Wild - Merve Noyan (keynote)

Multimodal retrieval modals (ex:ColPali)
Zero shot detection/classification: for any category (you can enter your own category)
Multimodal RAG: ColPali(R) -> qwen2-VL (R)
Fine tune/quantize if necessary.
Vision Language Models: HF has text-generation-inference.
Quantisation: BitsAndBytesConfig.
Parameters efficient fine tuning (PEFT).
Smol-vision: personal project.

### Run the benchmark they said, it will be fun they said - Vincent Warmerdam

Note: Look up Kaggle for bioQA dataset?
Joblib for parallelization (class Parallel): job generator as input - generator workflow works great.
Dropping id can speed up training time a lot
Caching is great, also for featurization
Use RandomizedCV for hyperparam search (with ParameterSampler)

### Polars 1.0 and beyond - Ritchie Vink

Version 1.0: there will be a GPU release.
Improved parquet performance.
Implemented correctness (error raised early, eg types).

### Alice in Open Source Land - Magdalena Kowalczuk

More of a personal tale than really technical, on tips to contribute to OS projects.
A good starting point is documentation.
[Narwhals](https://pypi.org/project/narwhals/): Python library that build a compatibility layer so that your dataframes are library-agnostic.

### GenAI Beyond Chat with RAG, Knowledge Graphs and Python - Martin O'Hanlon

Not a lot of new things when you already know about GraphRAG.A nice demo with LangChain and neo4j.
Note that the information you embed from nodes can be attributes, or neighbours.
GraphRAG is interesting with highly connected data - it performs better and is easier to store.
No word about how much more expensive it is in terms of compute.
Function of interest: LLM graph transformer (langchain) also used [here](https://github.com/neo4j-labs/llm-graph-builder)

[Material here](https://github.com/martinohanlon/pydata-ams-24)
[Free resources](graphacademy.neo4j.com)

### Roseman Labs - Python-powered encrypted AI - Niek Bouman

Data sharing is often the bottleneck (sounds familiar? :/).
Sharing Roseman labs architecture: multi-party computation.
It does not involved a trusted third party for storage.
[crandas](https://docs.rosemanlabs.com/latest/index.html): Pandas for encrypted data. You can join datasets without decrypting them, possibly run aggregates. Analysis always needs to be approved using a private key (e.g., not by the analyst, but by the data owner).

### Applied NLP in the age of Generative AI - Ines Montani (keynote)

Instructions:risk of data drift vs examples: nuanced, specific but labor intensive
Replace LLM with distilled task-specific components ==> more modular , small and fast , control over the data. Modularity and transparency.
For that you need a human in the loop: use llm to annotate for a specific task, use only the output to train a specific component (transfer learning). Then evaluate against baseline (llm?)
Refactoring code AND data
Evaluation of your model is similar to unit testing of your code, should be best practice
RIE (Retrieval via Information Extraction): alternative to RAG (see slide)
[Window knocking machine test](https://ines.io/blog/window-knocking-machine-test/): when you automate a task previously performed by human, are you building a knocker upper or an alarm clock? Think beyond chat bots
Chatting with data could replace other approaches but it depends on the scenario. One misconception is that you need to add many layers of abstraction - you still need product decisions.

Slides [here](https://speakerdeck.com/inesmontani/applied-nlp-in-the-age-of-generative-ai)


### The Odyssey of Hacking LLMs: Insights from Two Shipmates sailing in the LLM CTF @ SaTML 2024 - Thomas Fraunholz and Sandro Bauer

Defense of LLM: in a prompt appended to the general system prompt. Not the best as it can be hacked.
You could also use a filter, checking the LLM answer, truncating it if necessary (eg python filter). It is also possible to use an LLM filter.
This game setup reflects somehow the guardrails to setup to make sure the LLM does what it should do.
Problem: computationally expensive (LLM filter), latency. Also unharmful responses can be blocked, so you LLM might not be doing what it needs to anymore.
Compliance with EU AI act: ensure level of cybersecurity protection (art 55).
Attack:
- just ask
- encode
- jailbreak
Possible best defence: one or more fake passwords

### Terrible tokenizer troubles in large language models - Sander Land

Tokenisers have different vocab sizes.
Essentially impossible to change after training.
Nonsense “glitch” tokens coming from training dataset (eg Reddit usernames from very active profiles)
How to detect these tokens?
Use input embeddings: Rare tokens have smaller embeddings because of weights decay. Also a [paper](https://arxiv.org/pdf/2405.05417) about this.
Can help detect what model an API runs
Lack of spaces between words leads to longer tokens, can be a problem in languages like Chinese or Japanese.
Can be used for jailbreaking
A general tip to always look at your data.

### Polishing Python: Preventing Performance Corrosion with Rust - Mike Krause

[repo](https://github.com/MBKraus/pydata_payment_handler)

Python's flexibility comes at the cost of performance, due to its interpreted nature, dynamic typing, memory management and global interpreter lock (1 core at the time when you run code through the interpreter).
Rust = compiled language => optimized at compilation (ex: for loops to vectors).
But also: easy memory management with ownership rules.Think in scopes: every object has a single owner at a given time (vs in python you can assign one variable to another and both variables refer to the same object)
Foreign function interfacing = use Rust just for its speed and write the rest in Python.
High level abstractions do not introduce runtime overhead.
PyO3 package binds Rust objects to Python objects. Maturin does the rest by compiling the Rust code so that it can be used by Python.
More for custom use cases where no packages already exists that use Rust under the hood (ex for dataframes you'd use Polars).


### Pydiverse pipedag - Martin Trautmann

Competitor of Prefect (see tutorial above)
Wiring time (linking steps together) and runtime.
[slides](https://drive.google.com/file/d/1luFqwKsWFUghkyVcowvhRtdNEIryEcgv/view)

### How to measure a city - Francoise Provencher

Nice talk on topic conpletely unrelated to what we do. Some good points about picking metrics (see below).
What makes a city liveable?
Metric inspired by the 15min city concept with 6 indicators: counting on a fine grid what is accessible in 15min walk from a given point.
Good metric: simple balanced with faithful (to the spirit of what it is supposed to measure), sensitive (capturing changes that matter. Ex 1 shop out of 100 closes matters more it is the only grocery store), precise, cost effective
Be transparent about methodology and explicit about opinions (eg attributing scores) - justify opinions with research.
