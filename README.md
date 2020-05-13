DEVOPS ASSEMBLY LINES [TASK2]

Problem Statement :

Create a container image that’s has Jenkins installed using Dockerfile.

When we launch this image, it should automatically start the Jenkins service in the container.

Create a job chain of job1, job2, job3 and job4 using the build pipeline plugin in Jenkins.

Job1: Pull the GitHub repo automatically when some developers push the repo to GitHub.

Job2: By looking at the code or program file, Jenkins should automatically start the respective language interpreter install image container to deploy code ( eg. If code is of PHP, then Jenkins should start the container that has PHP already installed ).

Job3: Test your app if it is working or not.

Job4: If the app is not working, then send an email to the developer with error messages.

Create One extra job job5 for monitor: If the container where the app is running. fails due to any reason then this job should automatically start the container again.

SOLUTION :-

1)Creating a docker image which install jenkins image and jenkins service
![Screenshot (200)](https://user-images.githubusercontent.com/60460914/81862994-278f1200-9588-11ea-9ddd-8cba6625e605.png)


2)After building the docker then i run docker image which has jenins install in port no 8084



3)After that creating the job1(Note:github is the name there), job2, job3 and job4 by using build pipeline 
![Screenshot (198)](https://user-images.githubusercontent.com/60460914/81863013-2fe74d00-9588-11ea-9370-11157746950f.png)

4)Configuring Job1 task which download data and copy in the docker environment 
![Screenshot (209)](https://user-images.githubusercontent.com/60460914/81863472-e9462280-9588-11ea-896e-66621dc7287d.png)
![Screenshot (203)](https://user-images.githubusercontent.com/60460914/81863168-66bd6300-9588-11ea-8a3e-7de0424c01c3.png)



5)Configure the job2 task in my case i write python code which group the file accroding extension but i won't able to start docker inside another docker so i did whatever i know

![Screenshot (208)](https://user-images.githubusercontent.com/60460914/81863265-8f455d00-9588-11ea-8b52-5009a01ba837.png)
![Screenshot (205)](https://user-images.githubusercontent.com/60460914/81863273-93717a80-9588-11ea-82de-37feed6d6c82.png)


6)In job3 testing is to be done 
![Screenshot (204)](https://user-images.githubusercontent.com/60460914/81863307-9ff5d300-9588-11ea-9a86-e64c6181281b.png)

7)After this if job3 fail then send email

![Screenshot (206)](https://user-images.githubusercontent.com/60460914/81863314-a2582d00-9588-11ea-9934-91ab8f1a84b9.png)

8)This task in progress
