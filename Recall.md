---
tags:
  - 🌱
date: 18--Dec--2023
modified: 07--Jan--2024
aliases:
  - Sensitivity
  - TPR
  - True positive rate
---
# Recall
> [!question] Proportion of [[Relevance|Relevant]] docs in collection that are retrieved?

$$
Recall_u = \frac{tp_u}{tp_u + fn_u}
= \frac{Relevant Retrieved}{Relevant}
$$
Where:
- $tp_u$ is the number of items which are in the recommendation list of the user and have a rating >= relevant_threshold in its 'ground truth'
- $fn_u$ is the number of items which are NOT in the recommendation list of the user and have a rating >= relevant_threshold in its 'ground truth'
## [[RecSys]]
### Single user
Formula as above.
### Entire system
Depending if 'macro' average or 'micro' average has been chosen:
$$
Recall_{sys} - micro = \frac{\sum_{u \in U} tp_u}{\sum_{u \in U} tp_u + \sum_{u \in U} fn_u}
$$

$$
Recall_{sys} - macro = \frac{\sum_{u \in U} Recall_u}{|U|}
$$
## Properties
- Recall is a non-decreasing function of number of documents retrieved
    - As more documents retrieved, recall can only stay the same or increase
- Recall can always be 1 if all documents are retrieved since no non-relevant documents is missed
- [[Set-based measure]]

---
Links: [[Precision vs Recall]] - [[Information retrieval]]
