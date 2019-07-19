# Running a Spark Job on AWS Clustered Environment

AWS or Amazon Web Services is a cloud environment, which provides variety of different services at a cost. 

I am going to run a SPARK job using python on a dataset with 1 million records.
This is obviously a huge computation  and may take a little while, depending upon the number of clusters I would rent from AWS.

#### AWS has a per hour charge for each server on the cluster. Once the job is over, those servers must be manually terminated else the cost will increase by each passing hour, hense resulting in a huge $$. The per server cost is around 0.22$/hour and I am going to rent about 5 servers. Which will be divided as one master node and 4 executor nodes. 

It is obvious, that if this this script is run on a personal computer without any distribution applied to it, the Job will certainly fail. 

So, for this specific piece of code, a clustured environment is necessary. As a matter of fact, in Data Science, we tend to encounter Datasets which are often huge, if you don't have a clustered environment setup then AWS is a good option.
#### But only in a case if you pay extra attention to terminating your clusters after the job is over. 

Below are details about how I did it.

- [The Data Science Perspective](the-prespective.md)
- [The Dataset](the-dataset.md)
- [Understanding the Code](the-code.md)
- [The Terminal App](terminal-app.md)
- [Setting Up AWS](aws-setup.md)
- [Running the Spark Job](spark-job.md)
- [The Source File](same-movies.py)

