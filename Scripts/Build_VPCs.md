# Build VPCs


## EKS VPC
The EKS VPC is somewhat unique in that it has some specific tagging for kubernetes


```
MY_REGION=us-east-2
STACK_NAME=poceks
CFN_FILE=amazon-eks-vpc-3-private-subnets-tgw-subnets.yaml
curl -o $CFN_FILE https://raw.githubusercontent.com/cloudxabide/hybrid-poc/main/Files/$CFN_FILE
aws cloudformation create-stack --stack-name "${STACK_NAME}" \
  --template-body file://$CFN_FILE \
  --region ${MY_REGION} 
```

