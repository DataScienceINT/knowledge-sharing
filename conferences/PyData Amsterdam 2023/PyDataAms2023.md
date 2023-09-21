# PyData Amsterdam 2023
Marie Corradi

Most slides/content can be found in [this repo](https://github.com/yorickvP/PyDataContent/tree/master/2023%20-%20Amsterdam). Not all slides are there yet (as of 21/09/2023) but the owner is trying to gather them.


## Keynotes

- Vicki Boykis, "Build and keep your context window" (Day 1).  
A nice talk, sometimes hard to follow but luckily all notes are available. By the author on the 83-pages deep dive on embeddings I shared in the knowledge links. On the importance of knowing your context window (=memory, =cache). A nice practical advice I noted from there is to avoid bottlenecks in your pipeline, pre-compute what you need and put it into cache. I had a discussion with her afterwards on the difficulty of keeping track of your information. She mentioned the [Zettelkasten method](https://zettelkasten.de/introduction/), which I knew of but have not managed to implement properly yet. Maybe that's something we could work on as a group, or maybe someone has other tips.

- Robert Erdmann, "Python for imaging and Artificial Intelligence in cultural heritage" (Day 1).  
Unfortunately the notes are not available for this one, and I am not sure whether they will be. Robert Erdmann works at the Rijksmuseum and is part of the team that worked on the restauration of the Nightwatch. He showed more examples from his work, but that in particular was very coool to see. They took a 7B pixels resolution picture of the Nightwatch. Essentially a painting moves all the time, so they had to model the movement and automatically adjust the camera angle to be perfectly parallel to the painting every fraction of a millimeter.

- Katharine Jarmul, "AI without dystopia" (Day 2).  
Katharine works in data privacy and was essentially to shift the narrative from "tech giants have all the power" towards "what can you do as a person, as a community" and ideas to use your own power at your own scale to do some good. Mentioned the [Fairness through awareness](https://arxiv.org/pdf/1104.3913.pdf) paper, which I have yet to read but seems interesting. There were some copies of her [recent book on data privacy](https://www.oreilly.com/library/view/practical-data-privacy/9781098129453/) which I unfortunately haven't been able to score.

- Thomas Wolf and HuggingFace team, "Processing billions of tokens for training Large Language Models, tools and knowledge" (Day 2).  
They spoke a lot about the recently launched Falcon model, and the dataset they used to train it, [RefinedWed](https://huggingface.co/datasets/tiiuae/falcon-refinedweb). That dataset is a subset of CommonCrawl, where they applied what they called the Macrodata refinement pipeline. They used url filtering (to remove toxic content), language identification and filtering (keeping only English), some filtering based on deduplication and quality heuristics. Then large scale deduplication with Minhash so find similar documents and exact substring matching. 10% of CommonCrawl was left after that. I asked them whether they did anything else to remove toxicity from the corpus, but they did not and essentially pushed the problem back to end users wanting to refine the models, which I find a bit meh. They also obvously have no way to identify automatically generated content, but this was done pre-ChatGPT so hopefully is not overly polluted.  
A few other topics that were broached: Parameter-efficient fine-tuning (PEFT), QLoRA. With Spaces on the HuggingFace hub you can do a lot of things, demos, etc. Their [BLOOM model](https://bigscience.huggingface.co/blog/bloom) was evaluated and currently is the LLM that matched the most criteria in the draft EU AI act.

## Other talks

- Ziad Al Moubayed, "Reliable and Scalable ML Serving: Best Practices for Online Model Deployment" (Day 1).  
Do input/output type checks. Train and serve models in different files/scripts in order to reduce memory footprint.

- Feng Zhao, Tingting Qiao, "Graph Neural Networks for Real World Fraud Detection" (Day 1).  
They did graph creation with Spark, model training with DGL. They recommend to start with a shallow network. For explainability, they used neighbourhood analysis and business rules. Some details are on the [Adyen nowledge Hub](https://www.adyen.com/knowledge-hub/combating-marketplace-seller-fraud-with-graph-neural-networks).

- Emeli Dral, "Mind the language: how to monitor NLP and LLM in production" (Day 1).  
This was focused on LLM performing text-classification types of tasks, so maybe less interesting for us. One nice tip was to create descriptors on top of your raw data. You can then monitor the descriptors as numerical data.

- Krishi Sharna, "Innovation in the Age of Regulation: Federated Learning with Flower" (Day 2).  
In federated learning, the data lives on devices and is not dowloaded to a central server, which helps with privacy. Models are trained directly on the devices and their weights are sent to a central server where they are aggregated to form a global model. The disadvantage is that you are constrained by the client (device) resources, and that you cannot inspect or clean the raw data. In terms of tools, they considered Pysyft (but it was not research-friendly) and TensorFlow Federated (but it was not framework-agnostic) and ended up using Flower.

- Jakob Willisch, "The proof of the pudding is in the (way of) eating: quasi-experimental methods of causal inference and their practical pitfalls" (Day 2).  
Here I mainly noted some tools: DAGitty, CausalPy. Resources for causal inference are improving (it is very good in R but didn't used to be great in Python). DAGs are nice as they are reusable to show your assumptions to your shareholders.

## Tutorials

- Jetze Schuurmans, Roy van Santen, "Designing a Machine Learning system" (Day 1).  
They have a nice framework that we can re-use on systematic questions to answer when building an LM system.
![MLDS canvas](./mlsd.jpg)

- Panos Alexopoulos, "Mastering Knowledge Graph Modeling with Neo4j: A Practical Tutorial" (Day 2).  
Unfortunately this one was very theoretical and ended up not having room for practice. Still, it's nice to have some background knowledge on Semantic modelling. Materials are [here](https://drive.google.com/drive/folders/15ehGB9wK1T55-4qS9z6ko9TBWWXLwLFf)

## Other

I had a very good time chatting with the Explosion team. They gave us some tips for the WoE scoring annotation with Prodigy [here for mutiple categories](https://support.prodi.gy/t/creating-custom-labels-review-recipe-to-remove-noise-from-the-dataset/5863/4?u=ryanwesslen) and [here to have built-in answer verification](https://prodi.gy/docs/custom-recipes#validate_answer). Also, Prodigy Teams is finally out (in beta for now), yay!
