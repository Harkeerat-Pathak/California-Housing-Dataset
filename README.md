# California-Housing-Dataset


Here is the California housing data set, which contains data drawn from the 1990 U.S. Census. The following table provides descriptions, data ranges, and data types for each feature in the data set. A block group is the smallest geographical unit for which the U.S. Census Bureau publishes sample data (a block group typically has a population of 600 to 3,000 people). A household is a group of people residing within a home. Since the average number of rooms and bedrooms in this dataset are provided per household, these columns may take surprisingly large values for block groups with few households and many empty houses, such as vacation resorts. It can be downloaded/loaded using the :func:`sklearn.datasets.fetch_california_housing` function.

#### Frame the problem:

Is it supervised, unsupervised or reinforcement learning ? Is it a classification task, a regression task or something different ? Our problem is clearly a supervised learning task, because you have labeled input data. It is also clearly a regression task since you have to predict a numeric value.

![datatypes](https://user-images.githubusercontent.com/69766918/235444102-167b521f-0229-4cae-999a-93089f36ff7a.jpg)


![loading-csv](https://user-images.githubusercontent.com/69766918/235506090-ff07d99e-a9f4-4cd0-b088-6dec1505a6e0.jpg)


![head](https://user-images.githubusercontent.com/69766918/235506270-1f74bfb0-bf17-4135-a61b-423c79d7a31b.jpg)

#### 1.This data has metrics such as the population, median income, median housing price, and so on for each block group in California.

#### 2.A blockgroup typically has a population of 600 to 3,000 people.

#### 3.We will just call them “districts” for short.

![shape and dataframe](https://user-images.githubusercontent.com/69766918/235506685-2be6ee51-6b1f-4805-9dba-b11192714e3d.jpg)

#### Notice that there are 20,640 instances (entries) in the whole dataset. Also notice that the total_bedrooms attribute has only 20,433 non-null values which means that 207 districts don't have this feature. You can also see that ocean_proximity is not numerical and probably a categorical attribute. 

![statistical](https://user-images.githubusercontent.com/69766918/235507064-609cf037-ed52-4086-a41c-7928ecc0b8e8.jpg)

#### As Ocean_proximity is categorical and we con convert it into numeric values

![hot-encoding](https://user-images.githubusercontent.com/69766918/235507572-d6d8f97d-d513-4fbe-afb9-4ad0fa22104a.jpg)

## Data Visualization


### 1. Histogram

Histogram of all the numerical features has been plotted to give us an idea of the distribution of data into various bins. The x-axis gives the range in which the data falls that is the bin and the y-axis gives the count or the number of datasets in each bin.

![histogram](https://user-images.githubusercontent.com/69766918/235511503-206842fe-beb2-4a38-bbed-762f121aec94.jpg)

Now What I can Understand: 

1. longitude -  At -122 and -118 degrees are major houses
2. latitude - Looks correct, at 34 and 37 degrees of latitude are major houses.
3. housing median age -  At 35 and 15 are two peaks. are these years? max peak is at 50. does this mean major houses in each district are more than 50 years old?!? not very bell-shaped,
4. total rooms -  Most districts have around 3000 rooms 
 5. bedrooms - Looks like most districts have between 300-600 bedrooms
 6. population - most districts have population below 3000
 7.households - Most districts have around 100-500 households. peak is around 4800
 8. median income - very bell-shaped, good distribution, but is this income in dollars? There is no income above 15  most people have income between 2-5     
 9.median house value - Need to predict.Bell-shaped, at extreme right there is a surge, is y-axis dollars? does this mean most houses are above 500,000? 
   
   
