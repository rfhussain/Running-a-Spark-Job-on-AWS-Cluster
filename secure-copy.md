# Secure Copy Files to EC2

In order to run the files on the EC2 Instance, you have to copy the files to the Master Node. 
Below are the steps you need to perform for that. 

- You must have WinSCP or any appropriate tool to work for you. I am going to use WinSCP

- Open WinSCP

- Click on New Site

- Enter the ```Host Name``` which can be found once you click on SSH on the AWS Console Page, listing your Cluster Info (image Below)

![SSHImage](/images/host_name.PNG)

- Click on ```Advanced``` button as shown below

![SSHImage](/images/advance_1.PNG)

- Under the SSH from the left page, click on Authentication

- On the right page, Locate the PPK file which we've downloaded earlier from the AWS, this is ```Private key file:``` 

![SSHImage](/images/spark_key_winscp.PNG)


- Click on Login

- Once Logged in, copy the files needed

![SSHImage](/images/uploading.PNG)


- [Main Page](README.md)
- [The Source File](same-movies.py)


