# Maya's Machine Learning Portfolio

## EEG-PreProp-RAG, inspired by CodeRAG-Bench
> An EEG-specific RAG preprocessing model, inspired by the revolutionary project "CodeRAG-Bench: Can Retrieval Augment Code Generation?" and implemented using a RAG pipeline with open retrieval and code generation.


### 🔗 Links
**[Github Repository-](https://github.com/sanvi1855544/eeg_preprop_rag/blob/main/README.md)** includes README with implementation details.

**[NeurIPS Formatted Paper](https://github.com/sanvi1855544/eeg_preprop_rag/blob/main/CS_159_report.pdf)**

---

### Project Goals

Beginning as a final project for a Caltech class *CS 159: Advanced Topics in Machine Learning*, we were inspired to expand on the existing CodeRAG-Bench paper for EEG preprocessing specifically. EEG preprocessing is a foundational step in BCI Research, and yet is often overlooked, lacking a standardized protocol and often causing issues in downstream tasks. Our work focuses on building from the CODERAG-BENCH framework to create a benchmark tailored to EEG workflows. 

- Follows a RAG (Retrieval-Augmented Generation) structure.
- Draws on MNE documentation, public EEG-specific GitHub repositories, and domain-specific Stack Overflow discussions.
- Supports both canonical and open retrieval methods
- Evaluates robustness, syntax validity, and task achievement using GPT 3.5

---

### Retrieval Results

> <img width="570" height="150" alt="image" src="https://github.com/user-attachments/assets/e331122e-42cf-4109-b322-6ccaa34d8f80" />
We evaluate the canonical retrieval performance of our system in various standard metrics. These metrics measure the ranking quality (NDCG), the accuracy of top-ranked results (MRR), the ability to retrieve relevant documents among the top results (Recall), and the proportion of relevant documents in the top-ranked positions (Precision).
The combined dataset merges all the above sources together. While it has slightly lower metric values than some individual models, it yields overall strong results. The decline in scores is likely due to the increased size and added noise from variations in the query and corpus formatting and specificity. However, these factors also contribute to improved generalizability, which is crucial for accommodating a wider range of questions.

> <img width="550" height="294" alt="image" src="https://github.com/user-attachments/assets/6b8841e5-bc68-4c73-a238-8b2734619234" />

We used GPT-4o as a post-processing step to refine the initial generator output based on the retrieved context. We fed the user input describing a minimally processed signal along with the generator output to GPT-4o to get a post-processed script. We then applied that script to a 3 second segment from an EEG recording (Prof. Yisong and Geeling's decoding project, D10S2).
As seen in the above figure, there is good potential for one-shot preprocessing with RAG.




---


### Demo Notebooks

**[Canonical retrieval notebook](https://colab.research.google.com/drive/1mrqxg_F7dJNWkNi088yIs3XUYL8661Xv?usp=sharing)**
    
**[Open retrieval notebook](https://colab.research.google.com/drive/1atFGomyJCbrI2S-9OK4QvcANrtvGu9nM?usp=sharing)**
    
**[EEG data experiment notebook](https://colab.research.google.com/drive/1JXk2TGh3RdKOL02GBv8yX0XwuqZUNRbu?usp=sharing)**



___
