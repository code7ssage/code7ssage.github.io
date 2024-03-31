---
title: simple imputer
categories:
  - key_terms
toc: true
---

```python
imp = SimpleImputer(missing_values=np.nan, strategy='constant', fill_value=-9999)
imputed = imp.fit_transform(df2.loc[:, ['age', 'measurement']].values)
pd.DataFrame(imputed, columns=['age', 'measurement'])
```
- Imputer를 활용하여 결측치 채워넣기 (특정값)
```python
imp = SimpleImputer(missing_values=np.nan, strategy='mean')
imputed = imp.fit_transform(df2.loc[:, ['age', 'measurement']].values)
pd.DataFrame(imputed, columns=['age', 'measurement'])
```
- Imputer를 활용하여 결측치 채워넣기 (평균)
```python
imp = SimpleImputer(missing_values=np.nan, strategy='most_frequent')
imputed = imp.fit_transform(df2.loc[:, ['gender', 'education']].values)
pd.DataFrame(imputed, columns=['gender', 'education'])
```
- 최빈값(문자열) 사용