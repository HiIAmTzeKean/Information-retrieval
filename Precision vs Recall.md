---
tags:
  - 🌱
date: 18--Dec--2023
modified: 05--Jan--2024
---
# Precision vs Recall
Suppose a [[Classification]] task. Increasing the threshold of the prediction can allow more room for error in prediction of positive samples as negative samples. This will cause the [[Precision]] to increase since the false positive rate will be lower as the previously positive predictions would now be negative. However, doing so will cause more false negatives, [[Recall]] will decrease. The vice versa effect is the same.
A [[Precision-recall curve]] can be used to show the relation.

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/26/Precisionrecall.svg/350px-Precisionrecall.svg.png)](https://en.wikipedia.org/wiki/File:Precisionrecall.svg)
## Overcoming the trade off
- [[F score]]
- [[Accuracy]]

Reference: https://developers.google.com/machine-learning/crash-course/classification/precision-and-recall

---
Links:
