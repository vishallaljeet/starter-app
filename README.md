# socar test
Launch server and database instances:
a. Launch EC2 instances
b. Launch an RDS instance

adonis.cguth1piedzr.us-east-2.rds.amazonaws.com

c. Configure Elastic Beanstalk
d. Ensure that the requisite networking setup is set up as well.

For the above task I have launch ec2 instance and an RDS in public subnet. I have setup the VPC name as VPC-Test

VPC Test has 3 public and 3 private subnet with IGW and NAT attach to the subnet respectively.

For EBS I have selected the Docker as a platform and platform branch as Multi container Docker running, on which I have tried to setup of Deploy this node.js app https://github.com/socar-my/starter-app

We have 2 Dockerfile

Dockerfile-Adonis - Ubuntu as base OS on which I tried to create webserver and pushed to ECR "493849651063.dkr.ecr.us-east-2.amazonaws.com/socarproxy
Dockerfile-Nginx - I have used offical nginx image and same is uploaded to ECR 493849651063.dkr.ecr.us-east-2.amazonaws.com/nodejsproj

Deployed nodejs application on EBS, which can be access http://socartest-env.eba-pnfm2zrh.us-east-2.elasticbeanstalk.com/
