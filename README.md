# Amazon-Alexa
Building skills for Alexa

#Requirements
1. node > 6
2. aws account for lambda
3. postman for checking end points
4. Serverless - https://serverless.com/   serverless is a framework used for deploying and operating serverless architectures.

# Things to do in AWS

1. Login to AWS console.
2. Search for IAM.
3. On the left and side select `Users`
4. 

# Commands used

* This command is used to create a project.
```bash
serverless create --template aws-nodejs
```

* This command is used to test locally.
```bash
serverless invoke local -f hello

{
    "statusCode": 200,
    "body": "{\"message\":\"Go Serverless v1.0! Your function executed successfully!\",\"input\":\"\"}"
}
```

* This command is used to deploy the project.
* Before running you need to update .yml file `method: get` and 
```bash
serverless deploy
Serverless: Packaging service...
Serverless: Excluding development dependencies...
Serverless: Creating Stack...
Serverless: Checking Stack create progress...
.....
Serverless: Stack create finished...
Serverless: Uploading CloudFormation file to S3...
Serverless: Uploading artifacts...
Serverless: Uploading service .zip file to S3 (817.18 KB)...
Serverless: Validating template...
Serverless: Updating Stack...
Serverless: Checking Stack update progress...
..............................
Serverless: Stack update finished...
Service Information
service: hello-world
stage: dev
region: us-east-1
stack: hello-world-dev
api keys:
  None
endpoints:
  GET - https://no8rlbg37k.execute-api.us-east-1.amazonaws.com/dev/hello
functions:
  hello: hello-world-dev-hello
```