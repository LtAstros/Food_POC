# Food_POC


## Food 🍽️
This dataset has food recipes information from [food.com](food.com). It was originally scrapped and used by the authors to [this](https://cseweb.ucsd.edu/~jmcauley/pdfs/emnlp19c.pdf) recommender system paper.
- Note: While it is a great dataset that can help you build an exceptional project on your resume, it is quite large. And thus, you have the option to follow our guidelines below to process it into a smaller dataset for your analysis.

### Getting the Data
{:.no_toc}

The data is downloadable [here](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions/download?datasetVersionNumber=2). You need to download two datasets (`RAW_recipes.csv` and `RAW_interactions.csv`).

Optional steps to make it a smaller dataset if you do not have too much computation power on your computer:
1. Left merge the recipe and the interaction datasets together.
2. In the merged dataset, fill all 0 rating as `np.nan` because the minimum possible rating is 1, and those 0's were caused by people forgot to gave a rating while they left a comment.
3. Find the average rating per recipe and merge this information to the original recipe dataset.


A data dictionary is available at this [page](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions?select=RAW_recipes.csv).


### Sample Questions
{:.no_toc}

- What types of food that tends to have the most calories?
- What types of food that tends to have a higher average rating?
- What types of food that tends to be healthier (i.e. more protein, less carbs)?
- Do longer cooking time have an effect on the average rating?

### Cleaning and EDA
{:.no_toc}

Follow all of the steps in the [Requirement: Cleaning and EDA](#requirement-cleaning-and-eda-exploratory-data-analysis) section. Note:
- As stated in the data dictionary, the nutrition column stored data as lists in this order: `[calories (#), total fat (PDV), sugar (PDV) , sodium (PDV) , protein (PDV) , saturated fat (PDV) , and carbohydrates (PDV)]`. If you want to to use this data for your analysis, you may want to turn these lists into new columns for each of the values.
- You might also want to explore the dtypes for each column and change them into easier-to-handle dtypes if possible. (i.e. convert the data that looks like lists to actual lists or converting the dates into `datetime`)



### Assessment of Missingness
{:.no_toc}

Follow all of the steps in the [Requirement: Assessment of Missingness](#requirement-assessment-of-missingness) section.
- Note: there are only 3 columns in this dataset that contains missing values.

### Hypothesis Test
{:.no_toc}

Follow all of the steps in the [Requirement: Hypothesis Testing](#requirement-hypothesis-testing) section. You can use the sample questions for inspiration.
