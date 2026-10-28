
CloudWatch Agent:
AWS CloudWatch Agent is a tool to install on EC2 instance to collect system-level metrics and logs and send them to Amazon CloudWatch.

CloudWatch provides basic EC2 metrics, such as CPU utilization and network traffic.
but with cloudWatch Agent we can collect memory usage, disk usage, and application logs.

We installed the CloudWatch Agent on the EC2 instance and configured it to collect memory and disk utilization every 60 seconds. then attached an IAM role with require policy such CloudWatchAgentServerPolicy and CloudWatchLogFullaccess to allow the instance to send metrics to CloudWatch.

