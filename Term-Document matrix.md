---
tags:
  - 🌱
date: 24--Dec--2023
alias: 
modified: 02--Jan--2024
---
# Term-Document matrix
Create a term and document matrix such that we can simulate a vector space. Then we now have a vector for each term. To answer a query, [[Boolean retrieval model]] can be used.
## Challenge
- When the number of terms and document increase the size of the matrix expands by $T*D$
- Matrix generated would be very sparse since there are likely to be repeated words over each document
    - Assume each document had maximum of 1000 words
    - If T was 500k, and D was 1million
    - There would be at most $D*1000=1bilion$ possible 1 but the size of the matrix is $T*D$ which is far greater than 1 billion

---
Links:
