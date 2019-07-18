# The Data Set

In the example, I am going to use Movies & their Ratings Dataset. 
The Dataset is about users who've watched certain movies and provided their Ratings which can be from 1 to 5. 

For this example, I am going to download 1million movie ratings Dataset from the following website.
https://grouplens.org/
There are different Datasets available for download. Just click on “datasets” link on the top of the page.
You can download dataset with 100k records, and also with 10m records etc. In order to run a job with 10m record, even bigger clustered environment will be needed. 
Since this experiment will run on AWS environment, so from the cost saving perspective, 1m movie ratings dataset will be enough. While you are open to use the same code with 10m if you wish to, but there are costs incurred with every machine you rent. 
The cost structure will be shown later in the example. 

### The Dataset Structure:

In order to execute the script, we must understand the structure of the Dataset. With almost all Datasets, we have a readme.txt file available which will explain the structure and organization of the dataset, and hence a programmer is able to parse the file to manipulate the information contained in it.
There are two main files in the Dataset


