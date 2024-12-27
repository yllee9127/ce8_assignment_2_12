# ce8_assignment_2_12
Requirements:

Given a Lambda function that is triggered upon the creation of files in an S3 bucket, answer the following:
1. What is the purpose of the execution role on the Lambda function?
2. What is the purpose of the resource-based policy on the Lambda function?
3. If the function is needed to upload a file into an S3 bucket, describe (i.e no need for the actual policies)
   - What is the needed update on the execution role?
   - What is the new resource-based policy that needs to be added (if any)?

  
Answers:
1.	What is the purpose of the execution role on the Lambda function?

  	To provide permissions for the Lambda function to access AWS services.

2. What is the purpose of the resource-based policy on the Lambda function?
   
   To grant other AWS accounts and services permissions to access the Lambda function.

3. If the function is needed to upload a file into an S3 bucket, describe (i.e no need for the actual policies)
   - What is the needed update on the execution role?
     
     The execution role needs to have added access permission for the Lambda function to access S3 bucket resource with write access level (PutObject action).

   - What is the new resource-based policy that needs to be added (if any)?
     
     A new resource-based policy that allows S3 principal with the action to invoke the Lambda function (lambda:InvokeFunction) when one or more specific events occur (eg. Object removal event) will need to be added.

