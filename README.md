# AWS-Devops

## In this project I Used:

ECR = To Store the Docker Images

ECS = To deploy my application on Farget 

## First you need to clone this project on your machine :

* Create the REpository in ECR ,
* You Need to create IAM Role building the connection between EC2 to ECR to push image
  Attach the role to EC2 machine 
* You will get the commands to push the images to ECR from repository.


  <img width="1024" alt="Screenshot 2023-09-15 at 5 44 18 PM" src="https://github.com/hrbhardwaj/AWS-Devops/assets/131919525/c0f9fb8c-994b-4505-b0e1-22cfc25ea2a8">


* Now you Image is available to ECR repo:

<img width="1440" alt="Screenshot 2023-09-16 at 5 01 24 PM" src="https://github.com/hrbhardwaj/AWS-Devops/assets/131919525/0577850f-82e2-4298-a576-a431fe84ea48">


## Now Go to the ECS service :

Task is similar as Pod 
Service is similar as Deployment 


* Crate IAM Role to building connection Between ECR and ECS Fargate .
* Create Task Defination to deploy your Image on Farget  [Serverless]
* You have to provide the information that we usually give in our pod like image,port,env,vCPU,Memory etc

    Task Role : 
                    It is used to give the permmision to your application that can communicate with other service like S3 to send and pull the data
  
    Task Execution Role : 
                        It is used by ECS cluster to cummunicate with the other aws service like ECR to pull the images or providing metric                                     data to cloud watch.

  
* Now Create the cluster in which you define the type Farget and select the Task defination you created 
* Now you will get public IP of that taskb and you check with IP

  

  





