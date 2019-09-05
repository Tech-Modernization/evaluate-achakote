# API Gateway Example



### Deployment process.

* To create pipeline stack using below command.

`aws cloudformation create-stack --capabilities CAPABILITY_IAM --stack-name pipeline --parameters ParameterKey=GitHubOAuthToken,ParameterValue="XXXXX" --template-body file://pipeline.yaml`

This will create the pipeline and application stack.

* To Update the pipeline use below command.

`aws cloudformation update-stack --capabilities CAPABILITY_IAM --stack-name pipeline --parameters ParameterKey=GitHubOAuthToken,ParameterValue="XXXXX" --template-body file://pipeline.yaml`


### Future Improvements

1. Use Authorizers to authenticate API gateway, Resource Policy if necessary
2. Enable cloudwatch logs, Access logging
3. Stricter permissions on CodePipelineRole and CloudformationRole in pipeline.yaml
4. Add Tags
