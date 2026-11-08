## Cloud Watch:

Cloud Watch is nothing but the monitoring tool that provide realtime monitoring which is use to monitor AWS resources. such as health check, Cpu utilization, Memory utilization.

It collect & track matrix.
It collect monitor & Store logs.
Monitor AWS event.
Create Alarm.

Cloud Watch Alarm:

1. OK:
If the current value goes below threshold value.

2. In Alarm:
If the current value goes above threshold value.

3. Insufficient data:
It still collecting the data.


Amazon CloudWatch Events:

Amazon CloudWatch Events is a service in AWS that automatically detects when something happens in your AWS environment and triggers an action.

When an EC2 instance starts and stops, CloudWatch Events detects it.
Based on that event, it can trigger an action, such as sending a notification through SNS.
