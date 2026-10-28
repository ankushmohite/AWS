
## CloudWatch Agent:
AWS CloudWatch Agent is a tool to install on EC2 instance to collect system-level metrics and logs and send them to Amazon CloudWatch.

CloudWatch provides basic EC2 metrics, such as CPU utilization and network traffic.
but with cloudWatch Agent we can collect memory usage, disk usage, and application logs.

We installed the CloudWatch Agent on the EC2 instance and configured it to collect memory and disk utilization every 60 seconds. then attached an IAM role with require policy such CloudWatchAgentServerPolicy and CloudWatchLogFullaccess to allow the instance to send metrics to CloudWatch.



## amazon-cloudwatch-agent.

```bash
yum install amazon-cloudwatch-agent -y
```

`/opt/aws/amazon-cloudwatch-agent/etc/amazon-cloudwatch-agent.d`

Vi amazon-cloudwatch-agent.json

```json
{
  "logs": {
    "logs_collected": {
      "files": {
        "collect_list": [
          {
            "file_path": "/var/lib/docker/containers/*/*.log",
            "log_group_name": "docker-container-logs",
            "log_stream_name": "{instance_id}-docker",
            "timestamp_format": "%Y-%m-%dT%H:%M:%S"
          }
        ]
      }
    }
  }
}
```

```json
{
  "logs": {
    "logs_collected": {
      "files": {
        "collect_list": [
          {
            "file_path": "/var/lib/docker/containers/*/*.log",
            "log_group_name": "docker-container-logs",
            "log_stream_name": "{instance_id}-docker"
          }
        ]
      }
    }
  },

  "metrics": {
    "append_dimensions": {
      "InstanceId": "${aws:InstanceId}"
    },
    "metrics_collected": {
      "mem": {
        "measurement": [
          "mem_used_percent"
        ],
        "metrics_collection_interval": 60
      }
    }
  }
}
```
