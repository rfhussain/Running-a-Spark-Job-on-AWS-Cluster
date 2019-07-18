# Setting up AWS 

Please note that you are going to need to provide your Credit Card Number in order to complete the registration. I have registered and taken a developer plan, which costed me 29$ a month. 

You can also choose a “Basic” plan which will just work fine and you will only be charge for the Cluster you’ve rented for running the SPARC job. 

### Caution: Once you are done running your SPARK job on the AWS, you must shutdown (or terminate your cluster) or else, the charging will continue each and every second and you will end up billed for $$$. 

-	Go to https://aws.amazon.com/
-	Create an Amazon Web Services Account
-	Follow the instructions, and fill up your billing information and other details

You will receive email and the last step would be to complete your identification, that is you will have to provide your phone number, where a security code will be sent and you can take that code and enter in the website to complete your registration. 

Once done, Click on ```Sign In to the Console``` as shown in the picture below

![AWS Con](/images/sign_in_console.PNG)

On the AWS Console Page, under All Services, click on ```EMR``` which you can find under ```Analytics``` as shown below

![AWSEMR](/images/emr_analytics.png)

As mentioned earlier, it is not just Map Reduce, EMR is basically a managed hadoop framework, so it will bring up a hadoop cluster for you and it actually has SPARK as well. It actually uses the YARN component of hadoop as a Cluster Manager, that SPARK runs on top of. 

So We are going to click on EMR and get Nodes (Master Node & Client nodes), as many as we want. ```On Per hour Rent off course```

Once you've acquired all the required nodes, all you need to do is to login to the master node and copy all the required data in it and make sure that it is accessible from there and run it. 

##### We are going to need Putty on Windows platform to access the master node. 




