
ALB access logs.

There is a option in load balancer attribute section i.e monitoring access logs.
We enable access logs and select an S3 bucket with the required bucket policy. AWS ALB then stores access logs in S3, which we use to troubleshoot issues.


Step:1

Goto ALB Attributer Section. Then Enable edit option.

<img width="940" height="431" alt="image" src="https://github.com/user-attachments/assets/1239a4da-d092-4ee0-a2ca-f0fe0239cc64" />

<img width="940" height="380" alt="image" src="https://github.com/user-attachments/assets/a3637c23-9023-453b-8eea-52fed39fd766" />

Then Select Created S3 Bucket.

Optional.
✅ Use कब करें: जब आप चाहते हैं कि आपकी application हमेशा available रहे, भले ही WAF थोड़ी देर unavailable हो जाए।


<img width="940" height="194" alt="image" src="https://github.com/user-attachments/assets/09ec202b-6047-4302-8558-456a6d684f61" />

Step:2
Create a Private S3 bucket.

If you make private bucket. So you need to give permission policy to the S3 bucket.
because S3 bucket can’t take ALB logs.


<img width="940" height="188" alt="image" src="https://github.com/user-attachments/assets/cbebf8f5-721e-4696-a31a-f6261816e0c5" />


Refer Below link to give S3 bucket permission policy.

Enable access logs for your Application Load Balancer - Elastic Load Balancing

Step:3
Goto S3 bucket permission.


<img width="940" height="344" alt="image" src="https://github.com/user-attachments/assets/111a6be1-4cac-47ac-8138-0f90358121e3" />




