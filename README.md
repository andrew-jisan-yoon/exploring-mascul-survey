# Data Cleaning and Exploration on Masculinity Survey dataset
 Data source : https://github.com/fivethirtyeight/data/tree/master/masculinity-survey

#### -- Project status : Closed

## Project Objective
The purpose of this project is to demonstrate how to clean and explore a survey dataset. <br>
Survey datasets are, while very common, easy to get 'dirty' thus difficult to clean for machine learning projects. <br>
By cleaning and exploring the survey dataset, the author wants to have solid confidence in his data cleaning skills and prepare dataset to build future machine learning projects on.

### Data cleaning
Data cleaning is done in `cleaning-responses.ipynb` and `cleaning-survey.ipynb`. <br>

`cleaning-responses.ipynb` has data cleaning processes for `raw/raw-responses.csv`, which contains all 1,615 responses to the survey. <br>
Each row corresponds to one respondent and each column corresponds to either his response to a question or his demographic characteristic. <br>

`cleaning-survey.ipynb` has data cleaning processes for `raw/masculinity-survey.csv`, which contains the summary of the survey results. <br>
Each row corresponds to a survey question and each column corresponds to a demographic category.

### Data exploration
Data exploration is done in `exploring-dataset.ipynb`. <br>

To aid the exploration process, `exploring-dataset.ipynb` generates in the first step `seaborn.heatmap` of Theil's U statistic (aka. uncertainty coefficient) of survey responses. <br>
Theil's U statistic is an asymmetric measure of association between categorical features. <br>
This metric was chosen as a summary statistic in lieu of Pearson's P value, because `cleaned-responses.csv` turned out to have either boolean or categorical datatype. <br>

Another alternative metric for categorical data was Cramer's V statistic, but it was a symmetric measure that cannot capture dependency relations between features, therefore it was not an effective metric to guide exploratory process.

### Methods used
* Data cleaning
* Theil's U (aka. uncertainty coefficient)
* Data visualization
* Data extraction

### Technologies
* Python
* pandas
* jupyter
* tqdm
* seaborn
* numpy
* scipy
* RegEx
