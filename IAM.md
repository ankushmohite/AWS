
# AWS IAM

AWS IAM (Identity and Access Management) is an AWS service used to control who can access AWS resources and what actions they can perform.

## User
A user is an identity that represents a person.

## IAM User
An IAM User is a permanent identity that can have long-term credentials.

## IAM Role
An IAM Role provides temporary permissions. It is commonly used for service-to-service communication, such as allowing an EC2 instance to access an S3 bucket.


1. How can i give S3 bucket permission access to the user.

We will create S3 bucket permission polity with specify the bucket ARN. then allow required permission such as list object, view object, read object, Put and Get object permission. 
So, user can access S3 bucket securely without deleting any object.


2. How can i give S3 bucket permission access to the Ec2 instance. 

I create an IAM role for EC2. then attach S3 bucket permission polity with specify the bucket. then ARN. then assign the role to the EC2 instance. then instance can access S3 bucket securely.



<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/9ffe238e-6a3f-4d29-838b-e0ce7689274b" />


<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/b25747f3-0bdb-4f3c-ba4d-99d3cb32118d" />


<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/329a4654-fabc-4e2f-8438-371810e25ce9" />


<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/e098978d-83b1-44d1-ac77-1a5c2fbcab2d" />



