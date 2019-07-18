# Running a Spark Job on AWS Clustered Environment

AWS or Amazon Web Services is a cloud environment, which provides variety of different services at a cost. 

I am going to run a SPARK job using python on a dataset with 1 million records.
This is obviously a huge computation  and may take a little while, depending upon the number of clusters I would rent from AWS.

##### Once a cluster is up and running, we must make sure to stop it once the job is over, else the costing will continue on per hour basis and may result on a huge bill at the end of the month. If anyone want to try this on AWS, needs to be extra careful and pay attention on terminating the cluster once the job is done. The termination step will be illustrated in the article later on. 

It is obvious, that if this this script is run on a personal computer without any distribution applied to it, the Job will certainly fail. 

So, for this specific piece of code, a clustured environment is necessary. As a matter of fact, in Data Science, we tend to encounter Datasets which are often huge, and an example of running huge jobs using a MapReduce clustured environment is quite relevent.

Below is the step by step example of how I did it.

- [The Data Science Perspective](the-prespective.md)
- [The Dataset](the-dataset.md)
- [Setting Up AWS](aws-setup.md)
- [Understanding the Code](the-code.md)
- [Setting Up Local Ennvironment](local-setup.md)
- [The Spark Job](spark-job.md)
- [The Source File](same-movies.py)

