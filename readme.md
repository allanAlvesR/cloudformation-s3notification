# cloudformation-s3notification
 
Lambda deployed with cloudformation to add triggers for existing s3 buckets.
<br>** You can simply run the python code by yourself.
 
## Description
 
This Cloudformation deploys a lambda function that uses boto3 to add s3notification to a preexisting bucket.
The lambda receives a payload with the *bucket_name* and the *stack_name* and then searches the stack outputs for the *lambda_arn* and adds a notification to the bucket.
 
<br>** This stack assumes the permission on the target lambda function are already set. If you need to set the permissions uncomment the code on that adds the labmda:InvokeFunction permission.
<br>** You can add or change the permissions type. *[boto3 doc](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html?highlight=s3#bucketnotification)*
 
If you wan't to use only the code you should directly assign the *bucket_name* and *lambda_arn* values.
 

