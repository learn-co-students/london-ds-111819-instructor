Data Cleaning in Pandas
===
​
​<br />
**Course**: Data Science <br />
**Mod**: Module 1                    <br/>
**Topic**: Pandas 3 - Data Cleaning  <br/>
**Amount of time**: 90 minutes <br/>
**Author**: Miles Erickson
​
​
***
​
## Lesson Summary:
​
#### Topic:
Pandas 3 - Data Cleaning in Pandas
#### Learn.co material:
(link to github)
#### Prerequisite knowledge/Prework:
Pandas lessons 1 and 2
#### Learning goals for this lesson:
Students will be able to:

- 1. Describe a clean dataset
	- Explain Hadley Wickham's concept of "tidy" data
	- Describe the concept of an Analytics Base Table (ABT)
- 2. Handle missing and invalid values in a dataset
	- Describe when it is appropriate to discard vs. impute
	- Add an indicator feature before imputing missing values
- 3. Create a repeatable Python function to load and prepare raw data

#### Misconceptions:
- As a data scientist, I can expect to begin with a clean dataset.
- When we have missing or invalid data, we can just drop it.
- It is acceptable to modify the original raw data in the data cleaning process.
- Data cleaning is a one-time step at the beginning of a project. It does not need to be repeatable.

#### Materials
- Instructor jupyter notebook files (TODO link here)
- King County Real Estate dataset
	- [Real Property Sales](https://aqua.kingcounty.gov/extranet/assessor/Real%20Property%20Sales.zip)
	- [Residential Buildings](https://aqua.kingcounty.gov/extranet/assessor/Residential%20Building.zip)
- Student jupyter notebook files (TODO link here)

***

## Lesson Outline:

**Step**: Introduction and outline of lesson <br/>
**Time**: 5 min

_Goal/Scenario:_<br/>
As data scientists, we want to build a model to predict the sale price of a house in Seattle in 2019, based on its square footage. We know that the King County Department of Assessments has comprehensive data available on real property sales in the Seattle area. We need to prepare the data.

_Learning Goals in sequence:_<br/>

#### 1. Describe a clean dataset
- Explain Hadley Wickham's concept of "tidy" data
- Describe the concept of an Analytics Base Table (ABT)

#### 2. Handle missing and invalid values in a dataset
- Describe when it is appropriate to discard vs. impute
- Add an indicator feature before imputing missing values

#### 3. Create a repeatable Python function to load and prepare raw data
- Describe how to convert categorical fields into binary values
- Explain why `pd.get_dummies` is not repeatable on new data

**Step**: Activation <br/>
**Time**: 10 min

Discussion prompts:

- What happens if you try to open this dataset in Google Sheets or Excel? (note: as of Office ~2017 Excel is unable to load the Real Property Sales file)
- Can Pandas load the data? (Yes.)
- Where can we find the square footage of a house in this dataset? (A: in the Residential building file)
- Where can we find the sale prices of houses sold in 2019? (A: in the Real Property Sales file)

**Step**: Learning Goal 1: _Describe a clean dataset_ <br/>
**Time**: 20 min

_Demonstrate_: 10 min

- Slides: Clean and Tidy Data, definition and context (6 min) (TODO)
- Show what the dataset will look like after preparation -- 3 numeric columns: year sold, square footage, sale price (4 min)


_Application_: 5 min

- Think, pair, share: what are the key differences between the raw dataset and the clean dataset?

_Informal assessment_: 5 min <br/>

- Slides: 4-5 slides showing examples of a few rows of data (TODO).
	 - Is it tidy? (entire class)
    - If not, what could we do to to make it tidy? (give all students time to think, cold call)

**Step**: Learning Goal 2: _Handle missing and invalid values in a dataset_ <br/>
**Time**: 20 min

_Demonstrate_: 10 min <br/>

- Slides: Handling Missing Values (TODO)

Instructor demo: Students are asked to close their laptops, follow along, interrupt, ask questions.

- Load the dataset (two dataframes)
- Join the two dataframes (review from Pandas 2)
- Subset rows to sales from 2019
- Subset columns to square footage, sale price
- Identify suspicious values for sale price ($1 etc)
- Identify missing values for square footage

_Application_: 5 min <br/>

Think-pair-share: in this context, what's the best thing to do with the suspicious sale price values?

_Informal assessment_: 5 min <br/>

- You have a million rows of data, but 200 rows are missing the target value that you want to predict with your model. What's the best thing to do?

- You have a dataset with many columns, and nearly every row is missing data in one or two columns. What's a reasonable approach in this case?

**Step**: Learning Goal 3: _Create a repeatable Python function to load and prepare raw data_ <br/>
**Time**: 15 min

_Demonstrate_: 10 min <br/>

Point: A key difference between a data _analyst_ and a data _scientist_: scientists do _reproducible_ work. Whereas an analyst might or might not document data preparation steps, data scientists document their work _in code_.

Remind students that they are not expected to follow along and "keep up" at this point.

Demonstrate wrapping the code from above into a Python function that takes the raw dataframe as an argument, and returns the clean data.

_Application & Informal Assessment_: 5 min <br/>

- Why is it important for data scientists to document their data preparation steps _in code_?
- What role do (potentially familiar) graphical tools like Microsoft Excel play in this type of a workflow?


**Step**: Assessment<br/>
**Time**: 5 min<br/>

Introduce lab exercise w/ scaffolding (load/join complete): students pair on data preparation.

#TODO discuss with group: is this an appropriate use of this space?

**Step**: Reflection:  <br/>
**Time**: 5 min <br/>

* Review objectives
