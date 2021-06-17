# Proramming1
####  Final Assignment of Programming 1

Author: Behzad Barati

----
Research Question:
Is there any significant difference between tomato usage in food recipes of Asian and European countries? we measure which fraction of recipes which have Tomato as their ingredients as an indicator for showing popularity of Tomato for each continent.

----
Dataset:
RecipeNLG dataset is composed of Recipe1M dataset and other recipes which were added by RecipeNLG authors.
This dartaset is introduced in RecipeNLG paper and is avalilable at this website.
Preprocessing steps:

We load RecipeNLG dataset, but For better quality of data, I removed recipes which were gathered by RecipeNLG authors.
Some preprocessing actions also took place on dataset (in Preprocessing recipe_table section). so we ended up with almost 360K recipes. Then I used different Libraries to allocate each recipe to a country in order to answer our reseach question.
Hints:

1_ As our csv file is greater than 2 gigabytes, I prefer to use cloud services(here google colab). I uploaded RecipeNLG dataset in my google drive. It is public.
2_ If there is out of memory error in running "ProfileReport", please first re-install latest version of "pandas_profiling" library, then try "minimal=True" argument in "profileReport" for eliminating some calculations. (pip install https://github.com/pandas-profiling/pandas-profiling/archive/master.zip)

----
Summary for doing statistical analysis:

* The two independent samples are simple random samples from two distinct populations.
* sample sizes are large, the distributions are not important (need not be normal)
* The test comparing two independent population means with unknown and possibly unequal population standard deviations is called the Aspin-Welch t-test. This can be done by doing T-test and mentiond that variances are not equal.
----
The population standard deviations are not known. Let A be the subscript for Asian and E be the subscript for European recipes. Then, μA is the population mean for asian recipes and μE is the population mean for European. This is a test of two independent groups, two population means.

Random variable: xA-xE = difference in the sample mean amount of time Asian and European used tomato in their recipes.

H0: μg = μb  H0: μg – μb = 0

Ha: μg ≠ μb  Ha: μg – μb ≠ 0

As our p-value is very low (zero), we can conclude that our means are equal and there is significant difference between our two groups. 
