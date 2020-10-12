## 08/10 - Homework 01

### Researches about theory (R)
#### **1_R.** 
[Wikipedia](https://en.wikipedia.org/wiki/Statistical_population) describes Statistical population as follows
> In statistics, a population is a set of similar items or events which is of interest for some question or experiment. A statistical population can be a group of existing objects (e.g. the set of all stars within the Milky Way galaxy) or a hypothetical and potentially infinite group of objects conceived as a generalization from experience (e.g. the set of all possible hands in a game of poker). A common aim of statistical analysis is to produce information about some chosen population. 

So we can define statistical population as a set of similiar existing or hypotetical object/events which study of the related data seems interesting for question/experiments

In **descriptive statistics**, the population is intented to be a sample of a larger group (population) on wich features will be noted and organized and used for te data analysis.  

In **inferential statistics**, the population is also a sample of a larger population on wich data is harvested and used for the inference of a larger population.  

The main differneces in the two population samples is that:  
  - Descriptive Statistics analyzes data and describes statistics of the sample ONLY,  
  - On the other hand Inferential statistics aims to analyze data of a sample to make (as the name says) inference on the larger population.  
  
#### **2_R.**  
  -  We can describe **statistical attributes** as a specific characteristic of an object, like age, weigth or height;  
  - **statistical variables** on the other hand are logical sets of attributes that (as the name suggests) may vary, those can be conisdered a representation of attributes for a further data processing;
  - With the term **Dataset** we describe a collection of data organized (usually) as a table, each column corresponds to a *variable* and each row corresponds to a given member of the dataset.  
  
#### **3_R.**  
   - A **univariate dataset** consists in a single variable type dataset, so we will have a single column table containing just the variable we want to examine; For example, if we want to create a univariate dataset containing the weights of 10 apples we use the weight attribute of the apple as a variable and create the 1 column-10 rows dataset containing the data.
 - The number of occurence of the same data for a specific attribute in a variable is known as **frequency ditribution**; for example we have this weights array (in grams):  
 ```w={22.0, 32.2, 44.3, 32.2, 21.9, 32.3, 22.0}```  
 we know that the distribution of 32.2 is 3.  
 
  - Actually yes, if we have the distribution of every possible value in the dataset for a certain variable we could recreate the dataset, let's take the previous example about apple weights, if we know that:  
  ```22.0 = 2,  32.2 = 3, 44.2 = 1, 21.9 = 1 ```  
  We could easily recreate the univariate dataset.  
  If we had a frequency distribution divided by classes or grouped variables, it would be hard to recreate the original dataset, for example taking back the apple weights:  
    ``` 20-30 = 3, 31-40 = 3, 41-50=1```  
    it's actually a more synthetic way to create a frequency distribution but it makes impossible to define what the original data was.

 - The difference in the amount of data between the two is directly correlated to the variety of data, the dataset is a more organized version of the data, frequency distribution is just a concise version of the same data, if we have a distribution of 1 for each value we will have the exact same dataset just in a different notation, on the other hand, if we have high distribution of values we will end up with a briefer version of the dataset.

### Applications / Practice (A)
  1_A.
  - [C# zip file](https://drive.google.com/file/d/1R2cDsJLh_hcP5wOe_d0STyCQVivkWqmY/view?usp=sharing)  
  - [VB.NET zip file](https://drive.google.com/file/d/1NY1Byu0iRMpn7ZTiBgfmChd4ixgGHpZA/view?usp=sharing)  
    
  2_A.  
  3_A.
  - I've implemented the Drag&Drop function in both the programs at point 1_A 

### Researches about applications (RA)
  1_RA.  
  2_RA.  
