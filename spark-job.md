# Running the Spark Job

Now it's time to run the Spark Job
- Run the PuTTY.exe and in the left page, under the SSH, click on Auth.
- In the Right pane, select the PKK file which we've generated through the PuTTYGen.exe

![Putty](/images/putty.png)

![Putty](/images/putty2.png)

- Click on Session, in the left pane, and Copy paste the Host Entry as shown below.

![Putty](/images/SSH2.PNG)

- Click on ```Open```
- You will get the Spark Welcome Screen as below.

![Putty](/images/hadoop_ssh_conn.PNG)

- Now it's time to run the following command in the SSH shel. 

```
spark-submit --executor-memory 1g movie_sim-1m.py 260
```

- One done, you will see logs of logging data, and the Job will probably run about 5 ~ 15 minutes depending upon the servers you've rented. 
As I've rented around 5 servers, my Job will run for approx 10 minutes to get the results. 

and You will get the following output 

```
Top 10 similar movies for Wizard of Oz, The (1939)
Toy Story (1995)        score: 661      strength: 1545
Toy Story 2             score: 594      strength: 1264
...
...
```


