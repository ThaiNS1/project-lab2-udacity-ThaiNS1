# project-lab2-udacity-ThaiNS1
<!-- the command to create stacks -->
aws cloudformation create-stack --stack-name udacity-network \
    --template-body file://network.yml   \
    --parameters file://network-parameters.json  \
    --region=us-east-1

aws cloudformation create-stack --stack-name udacity-udagram \
    --template-body file://udagram.yml   \
    --parameters file://udagram-parameters.json  \
    --region us-east-1 \
    --capabilities CAPABILITY_IAM

<!-- link web -->
http://udaci-webse-dl79q6jjsxc8-994722410.us-east-1.elb.amazonaws.com/