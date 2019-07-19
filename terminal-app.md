# The Terminal Application

If you are on windows environment as I am, you are going to need a terminal application that will connect with the Cluster (the master node in the cluster to be specific)

For this, there are many applications but I've been using putty for long time and I would suggest to use PuTTY.

to download PuTTY, go to the following website. 

https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

and download the following two applications (64 or 32 bit as per your OS)
- putty.exe (The terminal app to connect to the AWS cluster)
- puttygen.exe (Convert the PEM file downloaded from AWS to the ppk file which can be used by putty.exe)

Once both the applications are downloaded, open the puttygen.exe and click on ```Load``` as shown in the following image

![PuttyGen](/images/putty_gen.png)

Locate the ```SPARKAWS.pem``` file which we've saved earlier (Please keep File-Type to All Types as puttygen.exe by default looks for a PPK file ) and Load it into PuttyGen.exe as shown below.

![PuttyGen](/images/putty_load.PNG)

Once you are done, the puttygen.exe would give you the following message:

```Successfully Loaded```

Click on ```Save Private Key``` button to generate the key/value pair. After doing that, we will have a .PPK file format which is underatable by PuTTY.exe and we are going to use this when connecting to the cluster.

![PuttyGen](/images/save_pkk.png)


