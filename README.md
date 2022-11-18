## Outline:

## Implement a Machine Learning model for predicting whether an SMS message is spam or not.
-Follow the following AWS tutorial on how to build and train a spam filter machine learning model using Amazon SageMaker: https://github.com/aws-samples/reinvent2018-srv404-lambda-sagemaker/ blob/master/training/README.md. 

-The resulting model should perform well on emails as well, which is what the rest of the assignment will focus on.  

-Deploy the resulting model to an endpoint (E1).  


## Implement an automatic spam tagging system.
-Create an S3 bucket (S1) that will store email files...

-Using SES, set up an email address, that upon receipt of an email it stores it in S3.  

-Confirm that the workflow is working by sending an email to that email address and seeing if the email information ends up in S3.  

-For any new email file that is stored in S3, trigger a Lambda function (LF1) that extracts the body of the email and uses the prediction endpoint (E1) to predict if the email is spam or not.

-You might want to strip out new line characters “\n” in the email body, to match the data format in the SMS dataset that the ML model was trained on.

-Reply to the sender of the email (it could be your email, the TA’s etc.) with a message as follows:
“We received your email sent at [EMAIL_RECEIVE_DATE] with the subject [EMAIL_SUBJECT].  

Here is a 240 character sample of the email body: [EMAIL_BODY]. 

The email was categorized as [CLASSIFICATION] with a [CLASSIFICATION_CONFIDENCE_SCORE]% confidence.”  

Replace each variable “[VAR]” with the corresponding value from the email and the prediction.  


## Create an AWS CloudFormation template for the automatic spam tagging system.

-Create a CloudFormation template (T1) to represent all the infrastructure resources (ex. Lambda, SES configuration, etc.) and permissions (IAM policies, roles, etc.).

## Architecture DIagram 

https://github.com/takhilabhinav/aws_email_spam/blob/main/Architecture/Screen%20Shot%202022-11-17%20at%2011.20.27%20PM.png
