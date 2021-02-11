# AWS CLI Command Cheatsheet

Useful commands for AWS CLI

Note: Append `--output text` to get text representation.

| Command | Description  |
|-------- | ------------ |
| `aws s3api list-buckets --query "Buckets[?starts_with(Name, 'cf-templates-')].Name"` | Query for CloudFormation template bucket |
| `aws cloudformation describe-stack-resources --stack-name <stackname> --query "StackResources[?LogicalResourceId=='<logicalid>'].PhysicalResourceId"` | Query for stack resource |
| `aws cloudformation describe-stacks --stack-name <stackname> --query "Stacks[0].Outputs[?OutputKey=='<outputname>'].OutputValue"` | Query for stack output |
