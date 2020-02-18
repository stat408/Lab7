# Lab7

Turn in one copy for each group. If group members are not present in class they will be required to complete their own lab to receive credit. Please turn in **both a DOC or PDF file and your R Markdown script**. 

## Lab Overview

This lab will use a subset of the Seattle Police 911 calls data set [http://math.montana.edu/ahoegh/teaching/stat408/datasets/Seattle_911_062016.csv](http://math.montana.edu/ahoegh/teaching/stat408/datasets/Seattle_911_062016.csv). 

```
library(readr)
seattle <- read_csv('http://math.montana.edu/ahoegh/teaching/stat408/datasets/Seattle_911_062016.csv')
```


## Data Wrangling

### Q1. (5 points)
Summarize the number of crimes cleared during each hour of the day (using the `Event.Clearance.Date`).

### Q2. (5 points)
How many crimes in the dataset are reported as `ROAD RAGE` (using the `Initial.Type.Description`).

## Data Visualization (10 points)

Create a figure telling a story from this dataset. Make sure to include appropriate axes, titles, and include an annotation.
