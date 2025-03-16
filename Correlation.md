---
tags:
  - 🌱
  - Statistics
  - Math
alias: Correlated
date: 14--Aug--2022
modified: 15--Jan--2024
---

# Correlation

![[correlation type.png]]

## [[RecSys]]
Every correlation method is implemented by the pandas library, so read its [documentation][pd_link] for more [pd_link](https://pandas.pydata.org/docs/reference/api/pandas.Series.corr.html)

The correlation metric is calculated as such for the **single user**:
$$
Corr_u = Corr(ranking_u, ideal\_ranking_u)
$$

Where:
- $ranking_u$ is ranking of the user
- $ideal\_ranking_u$ is the ideal ranking for the user

The ideal ranking is calculated based on the rating inside the *ground truth* of the user

The Correlation metric calculated for the **entire system** is simply the average of every $Corr$:
$$
Corr_{sys} = \frac{\sum_{u} Corr_u}{|U|}
$$
Where:
- $Corr_u$ is the correlation of the user $u$
- $U$ is the set of all users

---
Links: [[Bivariate data]]