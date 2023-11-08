---
theme: academic
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Presentation.
drawings:
  persist: false
transition: slide-left
title: TKDE23 Unifying Large Language Models and Knowledge Graphs - A Roadmap
mdc: true
# aspect ratio for the slides
aspectRatio: '16/9'
# real width of the canvas, unit in px
canvasWidth: 980
hideInToc: true
---

# <h2>TKDE23: Unifying Large Language Models and Knowledge Graphs: A Roadmap</h2>

Shirui Pan, Senior Member, IEEE, <br> Linhao Luo, Yufei Wang, Chen Chen, Jiapu Wang, Xindong Wu, Fellow, IEEE

Presented by Jixiang Xiong

---
layout: default
hideInToc: true
---

# Table of contents

<Toc maxDepth="1"></Toc>

---
layout: default
---

# Background

<Toc minDepth="2" maxDepth="2"></Toc>

---
transition: slide-left
level: 2
---

## Large Language Models (LLMs)

Most LLMs derive from the Transformer design, which contains the encoder and decoder modules empowered by a self-attention mechanism.

<div style="display: flex; justify-content: space-around; height: 70%; margin-top: 1%;">
<img src="/TransformerStructure.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 3
---

## Large Language Models (LLMs)

- **Encoder-only LLMs**

Training paradigm: predict the mask words in an input sentence

Downstream tasks: text classification and named entity recognition

Examples: BERT, ALBERT, RoBERTa, ELECTRA


- **Encoder-decoder LLMs**

Training paradigm: flexiable 

Downstream tasks: summariaztion, translation, and question answering

Examples: GLM-130B, T5, UL2, ST-MoE

- **Decoder-only LLMs**

Training paradigm: predict the next word in the sentence

Examples: Chat-GPT, GPT-4

---
transition: slide-left
layout: default
level: 3
---

## Large Language Models (LLMs)

<div style="display: flex; justify-content: space-around; height: 90%; margin-top: 2%;">
<img src="/LLMsInRecentYears.png" class="shadow rounded"/>
</div>

---
transition: slide-left
level: 2
---

## Knowledge Graphs (KGs)

Knowledge graphs (KGs) store structured knowledge as a collection of triples $KG = \{(h, r, t) \in E \times R \times E\}$, where $E$ and $R$ respectively denote the set of entities and relations.

---
transition: slide-left
layout: two-cols-header
level: 3
---

## Knowledge Graphs (KGs)

::left::

- **Encyclopedic Knowledge Graphs**

Most ubiquitous KGs, represent the general knowledge in real-world.

Examples: Wikidata, Freebase, Dbpedia, YAGO, NELL, CN-DBpedia, Vikidia, Knowledge Occean

- **Commonsense Knowledge Graphs**

Formulate the knowledge about daily concepts, help computers understand the meanings of words people use.

Examples: ConceptNet, ATOMIC, ASER, TransOMCS, CausalBanK

::right::

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 10%;">
<img src="/Encyclopoedic-Commonsense-KGs.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 3
---

## Knowledge Graphs (KGs)

::left::

- **Domain-specific Knowledge Graphs**

Represent knowledge in a specific domain, e.g., medical, biology, and finance; More accurate and reliable.

Examples: UMLS

- **Multi-modal Knowledge Graphs**

Represent facts in multiple modalities such as images, sounds, and videos.

Examples: IMGpedia, MMKG, Richpedia

<br>

::right::

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 2%;">
<img src="/DomainSpecific-MultiModal-KGs.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 2
---

## Representative Applications

<div style="display: flex; justify-content: space-around; width: 98%; margin-top: 2%;">
<img src="/RepresentativeApplications.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 2
---

## Pros and Cons

<div style="display: flex; justify-content: space-around; height: 90%; margin-top: 2%;">
<img src="/Pros-Cons.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 3
---

## Pros and Cons

**Hallucination**: generating factually incorrect statements.

<div style="display: flex; justify-content: space-around; height: 78%; margin-top: 1%;">
<img src="/HallucinationsInLLMs.png" class="shadow rounded"/>
</div>
<a href="https://arxiv.org/abs/2309.01219" style="display: flex; justify-content: space-around">
Arxiv: Siren's Song in the AI Ocean: A Survey on Hallucination in Large Language Models
</a>

---
transition: slide-left
layout: default
level: 1
---

# Roadmap & Categorization

<Toc minDepth="2" maxDepth="2"></Toc>

---
transition: slide-left
layout: default
level: 2
---

## Roadmap

<br>

<br>

<div style="display: flex; justify-content: space-around; height: 55%; margin-top: 1%;">
<img src="/Roadmap-Unifying.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 2
---

## Categorization

<div style="display: flex; justify-content: space-around; height: 95%; margin-top: 1%;">
<img src="/Categorization.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 1
---

# KG-enhanced LLMs

<Toc minDepth="2" maxDepth="2"></Toc>

---
transition: slide-left
hideInToc: true
layout: default
---

## KG-enhanced LLMs

<div style="display: flex; justify-content: space-around; height: 95%; margin-top: 1%;">
<img src="/KG-Enhanced-LLMs.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## KG-enhanced LLM Pre-training

::left::

- **Integrating KGs into Training Objective**

  - Approach 1: give higher masking probability to important entities

  - Approach 2: concat input text with entities in the text as the input

<br>
<br>
<br>
<br>
<br>
<br>

::right::

<div style="display: flex; justify-content: space-around; height: 70%; margin-top: 1%;">
<img src="/KG-LLMs-Pretraining-1.png" class="shadow rounded"/>
</div>

<div style="display: flex; justify-content: space-around;">
word-entity alignment training objective
</div>


---
transition: slide-left
layout: two-cols-header
level: 3
---

## KG-enhanced LLM Pre-training

::left::

<br>
<br>
<br>

- **Integrating KGs into LLM Inputs**

Introduce relevant knowledge sub-graph into the inputs of LLMs.

::right::

<div style="display: flex; justify-content: space-around; height: 85%; margin-top: 1%;">
<img src="/KG-LLMs-Pretraining-2.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 3
---

## KG-enhanced LLM Pre-training

::left::

<br>
<br>
<br>

- **Integrating KGs by Additional Fusion Modules**

Separately process the information from KGs and fuse them into LLMs.

<br>
<br>
<br>
<br>
<br>
<br>

::right::

<div style="display: flex; justify-content: space-around; height: 80%; margin-top: 1%;">
<img src="/KG-LLMs-Pretraining-3.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## KG-enhanced LLM Inference

::left::

<br>

- **Dynamic Knowledge Fusion**

Leverage a two-tower architecture where one separated module processes the text inputs and the other one processes the relevant knowledge graph inputs. Then, joint them together.

<br>
<br>
<br>
<br>
<br>
<br>

::right::

<div style="display: flex; justify-content: space-around; height: 65%; margin-top: 1%;">
<img src="/KG-LLMs-Inference-1.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 3
---

## KG-enhanced LLM Inference

::left::

<br>
<br>

- **Retrieval-Augmented Knowledge Fusion**

Combine non-parametric and parametric modules to handle the external knowledge.

<br>
<br>
<br>
<br>
<br>
<br>
<br>

::right::

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 1%;">
<img src="/KG-LLMs-Inference-2.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## KG-enhanced LLM Interpretability

::left::

<br>

- **KGs for LLM Probing**

Converts the facts in KGs into cloze statements by a predefined
prompt template and then use LLMs to predict the
missing entity. The prediction results are used to evaluate
the knowledge stored in LLMs.

<br>
<br>
<br>
<br>
<br>

::right::

<div style="display: flex; justify-content: space-around; height: 65%; margin-top: 1%;">
<img src="/KG-LLMs-Interpret-1.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 3
---

## KG-enhanced LLM Interpretability

::left::

<br>
<br>
<br>

- **KGs for LLM Analysis**

Explain the reasoning process of LLMs by extracting the graph structure from KGs.

Results: LLMs generate the missing factual more by the positionally closed words rather than the knowledge-dependent words.

Claim: LLMs are inadequate to memorize factual knowledge because of the inaccurate dependence.

<br>
<br>
<br>
<br>


::right::

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 20%;">
<img src="/KG-LLMs-Interpret-2.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 1
---

# LLM-augmented KGs

<Toc minDepth="2" maxDepth="2"></Toc>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## LLM-augmented KG Embedding

::left::

- **LLMs as Text Encoders**

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 1%;">
<img src="/LLM-KG-Embedding-1.png" class="shadow rounded"/>
</div>

<br>

::right::

- **LLMs for Joint Text and KG Embedding**

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 10%;">
<img src="/LLM-KG-Embedding-2.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## LLM-augmented KG Completion

::left::

- **LLM as Encoders (PaE)**

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 1%;">
<img src="/LLM-KG-Completion-1.png" class="shadow rounded"/>
</div>

<br>

::right::

- **LLM as Generators (PaG)**

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 3%;">
<img src="/LLM-KG-Completion-2.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## LLM-augmented KG Construction

<br>

::left::

- **End-to-End KG Construction**

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 1%;">
<img src="/LLM-KG-Construction-1.png" class="shadow rounded"/>
</div>

<br>

::right::

- **Distilling Knowledge Graphs from LLMs**

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 20%;">
<img src="/LLM-KG-Construction-2.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 2
---

## LLM-augmented KG-to-text Generation

<br>

- **Leveraging Knowledge from LLMs**

<div style="display: flex; justify-content: space-around; height: 80%; margin-top: 1%;">
<img src="/LLM-KG-KG2Text-Generation-1.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## LLM-augmented KG Question Answering


::left::

- LLMs as entity/relation extractors


- LLMs as answer reasoners

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

::right::



<div style="display: flex; justify-content: space-around; height: 75%; margin-top: 1%;">
<img src="/LLM-KG-KGQA.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 1
---

# Synergized LLMS + KGS

<Toc minDepth="2" maxDepth="2"></Toc>

---
transition: slide-left
layout: two-cols-header
level: 2
---

## Knowledge Representation

<br>

::left::

The knowledge in the text corpus is usually implicit and unstructured, while the knowledge in KGs is explicit and structured.

It is necessary to align the knowledge in the text corpus and KGs to represent them in a unified way.

::right::

<div style="display: flex; justify-content: space-around; width: 100%; margin-top: 0%;">
<img src="/LLM+KG-Representation.png" class="shadow rounded"/>
</div>

---
transition: slide-left
layout: default
level: 2
---

## Reasoning

- Question answering task: utilize LLMs to process the text question and guide the reasoning step on the KGs.

- Knowledge graph reasoning task: transform the conventional logical rules into a language sequence and then ask LLMs to reason the final outputs.

- Adopt LLMs to generate the logical query, which is executed on the KGs to obtain structural context. Last, the structural context is fused with textual information to generate the final output.


---
transition: slide-left
layout: default
level: 1
---

# Future Directions

<br>

- **KGs for Hallucination Detection in LLMs**

- **KGs for Editing Knowledge in LLMs**

- **KGs for Black-box LLMs Knowledge Injection**

- **Multi-Modal LLMs for KGs**

- **LLMs for Understanding KG Structure**

- **Synergized LLMs and KGs for Birectional Reasoning**

---
transition: slide-left
layout: center
hideInToc: true
---

# Thanks

