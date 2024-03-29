# Setting up AWS

Please note that you are going to need to provide your Credit Card Number in order to complete the registration. I have registered and taken a developer plan, which costed me 29$ a month. 

You can also choose a “Basic” plan which will just work fine and you will only be charge for the Cluster you’ve rented for running the SPARC job. 

### Caution: Once you are done running your SPARK job on the AWS, you must shutdown (or terminate your cluster) or else, the charging will continue each and every second and you will end up billed for $$$. 

-	Go to https://aws.amazon.com/
-	Create an Amazon Web Services Account
-	Follow the instructions, and fill up your billing information and other details
- In the last, identify your phone number by entering the code received via sms

##### Note : AWS charges 1$ from your account, which is not actually a charge but just an authorization. Sometimes this authorization may take up to 24 hours. As my registration took 2 hours to complete even though I immediately received notification from my bank that 1$ purchase has been done.  

Once done, Click on ```Sign In to the Console``` as shown in the picture below

![AWS Con](/images/sign_in_console.PNG)

Once the AWS instances are up and running, you need to actually connect to them in order to execute the job. For that, we need to have a public and private key pair. click on ```EC2``` to get the public and private key pair, as shown in the image below. These pair will help us sign in to the EMR cluster. 

![AWSEMR](/images/ec_2.PNG)

On the EC2 page, click on the Key Pairs as shown in the image below. This is to create a Key/value pair which we are going to use for authentication when connecting to the cluster, to execute our job. 

![AWSEMR](/images/key_pair.PNG)

On this page, click on ```Create Key Pair``` as shown in the image below. Provide the name of the Key Pair, as I've given the name ```SPARKAWS``` and this will automatically downloaded to your download folder. Make sure you keep this in a safe place because once generated and downloaded, you can not download it again. 

![AWSEMR](/images/pem_file.PNG)

At this point, you should Stop and Complete the step mentioned below. Because, Once you create a Cluster, it will be provisioned &  running. Once running, your charging will start. So better, make your remaining home work before you actually create a Cluster. 

- [The Terminal App](terminal-app.md)

On the AWS Console Page, under All Services, click on ```EMR``` which you can find under ```Analytics``` as shown below

![AWSEMR](/images/emr_analytics.png)

As mentioned earlier, it is not just Map Reduce, EMR is basically a managed hadoop framework, so it will bring up a hadoop cluster for you and it actually has SPARK as well. It actually uses the YARN component of hadoop as a Cluster Manager, that SPARK runs on top of. 

So We are going to click on EMR and get Nodes (Master Node & Client nodes), as many as we want. ```On Per hour Rent off course```

Click on ```Create Cluster``` as shown in the figure below.

![AWSEMR](/images/create_cluster.PNG)

You will go to the create cluster page, where I've selected the following settings. (see the image below)
m4.xlarge instance is going to cost me around 0.2$ per hour, and I am going to rent 5 servers.
### So for 1 hour I am going to charge for 1$

![AWSEMR](/images/create_cluster2.PNG)

Click on``` Create Cluster```

You will get the following screeen

![AWSEMR](/images/aws_cluster_struc.png)

As you can see that, AWS has auto configured 1 Master node and 4 Core (executor nodes) on the cluster.
Also, the status shows as ```Provisioning```, which means that AWS is looking for available servers on their huge data center to provision for our job as they become available.

#### The whole process of up and running may take up to 5 minutes. 

Once done, you will get the following status.

![AWSEMR](/images/cluster_running.PNG)

Once you've acquired all the required nodes, all you need to do is to login to the master node and copy all the required data in it and make sure that it is accessible from there and run it. 

- [Main Page](README.md)
- [FTP Your Files](secure-copy.md)
