---
tags:
  - 🌱
date: 18--Dec--2023
modified: 06--Jan--2024
---
# Precision
> [!question] Proportion of documents [[Relevance|relevant]] to user information need ?

$$
Precision_u = \frac{tp_u}{tp_u + fp_u}
= \frac{Relevant}{Retrieved}
$$

Where:
- $tp_u$ is the number of items which are in the recommendation list of the user and have a rating >= relevant_threshold in its 'ground truth'
- $fp_u$ is the number of items which are in the recommendation list of the user and have a rating < relevant_threshold in its 'ground truth'
## Properties
- [[Set-based measure]]
## [[RecSys]]
### Single user
Formula is as above
### Entire system
Depending if 'macro' average or 'micro' average has been chosen:

$$ 
Precision_{sys} - micro = \frac{\sum_{u \in U} tp_u}{\sum_{u \in U} tp_u + \sum_{u \in U} fp_u}
$$
#### System Macro
Also known as Average precision (AP)
$$
Precision_{\text{sys-macro}} = \frac{\sum_{u \in U} Precision_u}{|U|}
$$
## Precision at K
### Advantage 
- Not requiring estimate of size of set of relevant documents 
### Disadvantage
- Being least stable across different evaluation metric
- Does not average well across different queries since the total number of relevant documents for a query affects the [[Precision]]
    - In the case of where K=10 but there are only 5 relevant document, [precision is penalised](https://stackoverflow.com/questions/46374405/precision-at-k-when-fewer-than-k-documents-are-retrieved)
## R-precision
Requires a set of known relevant documents $Rel$ to calculate precision of top $Rel$ documents returned.
$$\text{R-precision}=\frac{r}{Rel}$$
Then, the [[Recall]] would also follow the same equation $\frac{r}{Rel}$.
### Advantage
- Measures a single point on the [[Precision-recall curve]]
- Highly correlated to [[Mean average precision]]

---
Links: [[Precision vs Recall]] - [[Information retrieval]]
