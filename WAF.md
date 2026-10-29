## WAF.

AWS WAF stands for Web Application Firewall. It protects web applications from common web attacks such as SQL injection, DDoS attacks and unwanted traffic.

We create a Web ACL, rules and IP sets. In IP sets, we specify CIDR blocks to allow or block. We can also create rules to inspect HTTP headers and block unwanted requests.

We check LoadBalancer logs that store in S3 bucket. then we decide for which CIDER range we want to block.
