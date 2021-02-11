# AWS CLI Command Cheatsheet

Useful commands to use with the AWS CLI.

**Note: Append `--output text` to get text representation.**

---
## CloudFormation

#### Query for CloudFormation template bucket
`aws s3api list-buckets --query "Buckets[?starts_with(Name, 'cf-templates-')].Name"`

---
## S3

#### Query for CloudFormation Stack Resource
`aws cloudformation describe-stack-resources --stack-name <stackname> --query "StackResources[?LogicalResourceId=='<logicalid>'].PhysicalResourceId"`

#### Query for CloudFormation Stack Output
`aws cloudformation describe-stacks --stack-name <stackname> --query "Stacks[0].Outputs[?OutputKey=='<outputname>'].OutputValue"`
