# Route53:

Route53 is a domain name service use to and manage domain.

**Public Hosted Zone:** determine to route traffic on the internet.

**Private Hosted Zone:** determine to route traffic on the VPC.

1. **Simple routing:** Routes all traffic to single IP adress.
2. **Weight routing:** distribute traffic across mutiple resources.
3. **Latency routing:** Use to provide low latency. To route traffic nearest region.
4. **Failover routing:** Provide high availability to switch traffic. If the primary fail.

# ACM:

Create a request to add domain name --> DNS Validation --> RSA2048.

# ECS:

1. **Create a Cluster (Region specific)**

First we will give the name then select namespace.

AWS Farget.

2. **Create Task defination:**

How docker container should run on ECS.

we can define launch type farget --> CPU --> Task execution role --> Docker image --> port.

3. **ECS Service:**

Service basically use to manage the deploment and scalling task across ECS Cluster.

So, we can define launch type, Task defination revision, LoadBalancer then Auto-scalling group.

5. **Change Image:**

Goto task defination --> create new revision --> change image --> update service.

click on force new deploment and update.
