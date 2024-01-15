---
tags:
  - 🌱
date: 25--Dec--2023
alias: 
modified: 25--Dec--2023
---
# Biword index
Like a [[Term-Document matrix]], but each term is now made of 2 terms. Phrases would then be search on a basis of 2 terms.
## Challenge
False positives could be returned. For longer phrases the check on the continuous biword cannot guarantee that false results might be returned.
For example "stanford university school", then the biword would be "stanford university" and "university school". Without actually checking the documents, we cannot guarantee correctness as other terms might match.

---
Links:
