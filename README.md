## Outline:

## Implement a Machine Learning model for predicting whether an SMS message is spam or not.
-Follow the following AWS tutorial on how to build and train a spam filter machine learning model using Amazon SageMaker: https://github.com/aws-samples/reinvent2018-srv404-lambda-sagemaker/ blob/master/training/README.md. 

-The resulting model should perform well on emails as well, which is what the rest of the assignment will focus on.  

-Deploy the resulting model to an endpoint (E1).  


## Implement an automatic spam tagging system.
-Create an S3 bucket (S1) that will store email files...

-Using SES, set up an email address, that upon receipt of an email it stores it in S3.  

-Confirm that the workflow is working by sending an email to that email address and seeing if the email information ends up in S3.  

## 
