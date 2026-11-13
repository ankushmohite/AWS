## AWS CloudTrail.

AWS CloudTrail keeps a record of all activities happening in your AWS account.
In simple words, keeps a record of who performed which action, at what time, and from which location in your AWS account.



1. Management Events
Used to track activities like creating, deleting, or changing AWS resources.

Example: Creating or deleting an EC2 instance.
2. Data Events
Used to track activities happening inside AWS resources.

Example: Uploading or downloading files from an S3 bucket.
3. Insight Events
Used to identify unusual activities in your AWS account.

Example: Suddenly, someone creates many EC2 instances.



## CloudWatch Setup:
First, we create a topic and suscriber for mail.

Then, we create a CloudWatch Alarm. In the alarm, we define the EC2 instance ID, metric (CPU, Memory, etc.), threshold value, and alarm condition.

Next, we create a CloudWatch Dashboard to visualize metrics like CPU utilization, memory, and disk usage.
After that we create a cloudwatch event, in that event we create a rule and setup a multiple action target. target lets say SNS topic.

