# The Summary

Setting up AWS and running your job there can be challanging especially when you are doing it for the first time. 

Before I start with the steps, I am summarizing all what needs to be done in order to execute the job successfully. 

### - Make an AWS account
Making an AWS account, at times can be a lengthy process, may be your payment didn't go through or you need to contact your bank to authorize payments etc. 
While the payment will be just 1$ authorization, not a real charge.

### - Download PuTTY.exe and PuTTYGEN.exe
```PuTTYGEN.exe``` will be used for converting your Public Private Key pair to .MKK file format, which is understandable for both PuTTY.exe and WinSCP
```PuTTY.exe``` will be used as a terminal on Windows to actually connect to the master node on AWS and run the Job
 
### - Download WinSCP 
This will be used to ftp files on the master server

### - Run your code locally on a subset of actual Dataset  
If you directly run your script on the AWS server, you need to know that one ```m4.xlarge server``` will cost you around 0.2$ per hour. 
If you face any coding error or any other issue, it will unnecessarily increase your rented time. It is always better to experiment the code before you actually play on Cloud.

### - Generate Public/Private Key pair (which will be used for both PuTTY.exe and WinSCP
The public private key generation is an authentication process, which is standard, as you know

### - FTP the code/data ```ratings.dat``` in same DIR 
The ```ratings.dat``` file, needs to be placed in HDFS folder, as sometimes the code doesn't read the relative path on the server, rather it will work and read the file from HDFS
Below is how you are going to copy the file on the HDFS folder
```
hadoop fs mkdir yourdirname
hadoop fs -put ./ratings.dat yourdirname
hadoop fs -ls yourdirname
```

### - Rent the Clusters
Once all of the above pre-requisites are done, only then you are going to order servers.

#### Important: You also need to enable SSH in your node security, else your clusters will not accept inbound connections either from PuTTY.exe or WinwSCP
This documentation is not properly mentioned in AWS by default. Rather, you have to do search through their Knowledge Base and FAQs to get a clue on how you are going to enable SSH protocol inbound security 
In summary, you have to list all your nodes, when they are up and running (step are mentioned in Setting Up AWS) and click on each node one by one and the ```Description``` section, which will appear only when you select the node, you will have to click on Security Group under Security Groups field to add additionall SSH security


### - Connect to the Master Node, Execute the Script
You will use PuTTY.exe to connect, and detailed procedures will come later in this article.

### - Terminate the Nodes
You must terminate the nodes, else the billing will continue and it will result in huge $$


- [Main Page](README.md)
- [Data Science Perspective](the-prespective.md)
