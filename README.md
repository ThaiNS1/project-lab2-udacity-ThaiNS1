# project-lab2-udacity-ThaiNS1

1. link web
http://udaci-webse-dl79q6jjsxc8-994722410.us-east-1.elb.amazonaws.com/

2. the command to create stacks
aws cloudformation create-stack --stack-name udacity-network \
    --template-body file://network.yml   \
    --parameters file://network-parameters.json  \
    --region=us-east-1

aws cloudformation create-stack --stack-name udacity-udagram \
    --template-body file://udagram.yml   \
    --parameters file://udagram-parameters.json  \
    --region us-east-1 \
    --capabilities CAPABILITY_IAM

3. Infrastructure Diagram
![Alt text](image-2.png)

create 2 stacks for network-infra and udagram-infra:
![Alt text](image-15.png)

4. Parameters
![Alt text](image.png)
![Alt text](image-1.png)

5. Security Groups
![Alt text](image-3.png)

6. Resources
-LoadBalancer:
![Alt text](image-4.png)
-Launch Template:
![Alt text](image-5.png)
-AutoScaling group a health check:
![Alt text](image-6.png)
-The Load Balancer will have a Listener rule associated with the same target group:
![Alt text](image-7.png)
-Port 80 should be used in Security groups, health checks and listeners associated with the load balancer:
![Alt text](image-8.png)
![Alt text](image-9.png)
-Auto-Scaling should be using PRIV-NET ( private subnets ) for their auto-scaling instances:
![Alt text](image-10.png)
-Instance, The machine should have 10 GB or more of disk and should be a t3.small or better (Here is T3.medium)
![Alt text](image-11.png)
![Alt text](image-12.png)
![Alt text](image-13.png)

7. Outputs:
http://udaci-webse-dl79q6jjsxc8-994722410.us-east-1.elb.amazonaws.com/
![Alt text](image-14.png)