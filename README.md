# Running a Spark Job on AWS Clustered Environment

AWS or Amazon Web Services is a rented cloud environment, which provides many services at the cloud environment. 

I am going to run a python script using the spark engine for python on a dataset with 1 million records.
This is obviously a huge computation job and may take up to 15 minutes, depending upon the number of clusters I would rent.

##### A word of caution to those who are not accustomed to using the AWS before or who are not confident of carefully managing the cloud platform, is that you can just go through the article to get an idea of how AWS EC2 works. As a little carelessness in this case may cost you $$$. 

It is obvious, that if this this script is run on a personal computer without any distribution applied to it, the Job will certainly fail. 

So, for this specific piece of code, a clustured environment is necessary. As a matter of fact, in assignments pertaining to Data Science, we tend to encounter Datasets which are often huge, and an example of running huge jobs using a MapReduce clustured environment is quite relevent.

The detailed Steps for setting up AWS as well as preparing the script and Dataset will follow.

- [The Data Science Perspective](the-prespective.md)
- [The Dataset](the-dataset.md)
- [Setting Up AWS](aws-setup.md)
- [Understanding the Code](the-code.md)
- [Setting Up Local Ennvironment](local-setup.md)
- [The Spark Job](spark-job.md)
- [The Source File](same-movies.py)

