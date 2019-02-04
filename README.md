# Getting To Know Any Dataset In 4 Lines Of Python
<br/>

## A Dataset And a Person Walk Into a Bar

<img src="https://github.com/eyaltrabelsi/exploring_any_dataset_in_4_lines_of_python/blob/master/slides/RESOURCES/Get_to_know_data.png" width="400" height="300"/>


<img src="https://github.com/eyaltrabelsi/exploring_any_dataset_in_4_lines_of_python/blob/master/slides/RESOURCES/Get_to_know_data2.png" width="400" height="300"/>


## Whats Problematic?

#### - Time Consumming

#### - Its Manual and Not Fun

#### - Error Prone

#### - Many Skills Required

<br/><br/>
## Data Profiling Definition

![](https://github.com/eyaltrabelsi/exploring_any_dataset_in_4_lines_of_python/blob/master/slides/RESOURCES/data-profiling-definition.jpg)

<br/><br/>
## Data Profiling steps

1. Managing the input.
1. Performing the computation.
1. Managing the output.


```python
import pandas as pd
import pandas_profiling

df = pd.read_csv("data/VERY_MYSTERIOUS_AND_INTRESTING_DATASET_1.csv")
pandas_profiling.ProfileReport(df)\
                .to_file("reports/VERY_INTRESTING_DATASET_SUMMARY_1.html")
```

<br/>

Pandas allow to read into memory diffrent dataset types like:
- [Excel](https://pandas.pydata.org/pandas-docs/stable/api.html#excel)
- [Feather](https://pandas.pydata.org/pandas-docs/stable/api.html#feather)
- [CSV](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_csv.html)
- [Parquet](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_parquet.html)
- [Databases](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_sql.html)
- [More](http://pandas.pydata.org/pandas-docs/stable/api.html#input-output)         

<br/><br/>
## Report Results

![](https://github.com/eyaltrabelsi/exploring_any_dataset_in_4_lines_of_python/blob/master/slides/RESOURCES/unicorn-characters-who-are-doing-dubbing_36924-5.jpg)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[CLICK FOR MAGIC](reports/VERY_INTRESTING_DATASET_SUMMARY_1.html)

<br/><br/>
## No Silver bullet

- Pandas profiling SHINES on non-nested datasets, can be fixed by 
  [Flatten nested datasets](https://www.kaggle.com/jboysen/quick-tutorial-flatten-nested-json-in-pandas).


- Pandas requires a lot of RAM, can be fixed by [Sampling](https://www.statisticssolutions.com/sample-size-calculation-and-sample-size-justification/sampling/).


- Input should be [successfully Loaded](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.head.html).

- Pandas profiling doesnt support all profile tasks. :( 

- Pandas profiling treat ordinal columns as categorical. :(

<br/><br/>
## Installations

- [Install Python](https://www.anaconda.com/download/#macos)
- [Install pandas-profiling](https://github.com/pandas-profiling/pandas-profiling)                   

<br/><br/>
## Honorable Mention Packages

[pydqc](https://github.com/SauceCat/pydqc/):
- Data summary report for table.
- Summarize difference between two data tables (useful for comparing training set with test set, comparing the same data table from two different snapshot dates, etc.)


[missingno](https://github.com/ResidentMario/missingno):
- Missing data visualization module for Python.

<br/><br/>
## A lot of Theoretical [Stuff](https://www.researchgate.net/publication/277561530_Profiling_relational_data_a_survey)

![](http://s.quickmeme.com/img/5d/5d01b9deb8310756060ec054bcbaa48684c4b35333a4cba2bd54c516d9f52e59.jpg)

