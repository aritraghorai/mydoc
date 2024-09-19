---
{"dg-publish":true,"permalink":"/notes/learning/courses/advance-llm/python-for-ml/data-preprocessing/","title":"Data Preprocessing"}
---

# Handling missing values
There are two option if there are any missing values
1. Remove entire row
2. Fill the missing values
    1. Uni variate fill - Mean,Average,End of distribution
    2. Multi Variate fill - Knn Imputer,Itarative Imputer

### Cca - (Complete case analysis) 
```vid
https://www.youtube.com/watch?v=aUnNWZorGmk
```
```vid
https://www.youtube.com/watch?v=P_iMSYQnqac
```

It is also called list wise deletion where values of any variable is missing.
We will doing if the values are randomly missing.**Missing Completely at Random**
#### Disadvantage
- It can delete large portion of the data.
- Model not know how to handle missing data.
#### When we should use
- Data should not missing at random.
- There should not be more than 5% missing data.





