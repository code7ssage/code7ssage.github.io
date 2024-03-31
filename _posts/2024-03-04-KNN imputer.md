---
title: KNN imputer
categories:
  - key_terms
toc: true
---

```python
knn_imp = KNNImputer(n_neighbors=2, weights="uniform")
imputed = knn_imp.fit_transform(df2.loc[:, ['age', 'measurement']].values)
pd.DataFrame(imputed, columns=['age', 'measurement'])
```
- Imputer를 활용하여 결측치 채워넣기 (n_neighbor)