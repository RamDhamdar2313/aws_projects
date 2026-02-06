Straight, tight, interview-ready. Memorize these.

---

##  AWS Auto Scaling 

1. **What is AWS Auto Scaling?**
*  Automatically adds or removes EC2 instances based on demand to maintain performance and reduce cost.

2. **Why is Auto Scaling used?**
*  To ensure high availability, fault tolerance, and cost optimization.

3. **What is an Auto Scaling Group (ASG)?**
*  A logical group of EC2 instances managed together with min, max, and desired capacity.

4. **What is a Launch Template?**
*  A configuration template that defines how new EC2 instances are launched.

5. **Why are Launch Templates preferred over Launch Configurations?**
*  They support versioning and advanced features and are the modern standard.

6. **What triggers Auto Scaling actions?**
*  CloudWatch metrics such as CPU utilization, network traffic, or custom metrics.

7. **What is scale-out?**
*  Adding EC2 instances when demand increases.

8. **What is scale-in?**
*  Removing EC2 instances when demand decreases.

9. **What is Target Tracking scaling?**
*  A scaling method that maintains a metric at a target value automatically.

10. **What is Step Scaling?**
* Scaling based on how far a metric deviates from a threshold.

11. **What is Simple Scaling?**
* A basic alarm-based scaling method with cooldown periods.

12. **What is desired capacity in ASG?**
* The number of EC2 instances Auto Scaling tries to maintain.

13. **What is minimum capacity?**
* The lowest number of instances an ASG will ever run.

14. **What is maximum capacity?**
* The highest number of instances an ASG can scale up to.

15. **What happens when an instance fails a health check?**
* Auto Scaling terminates it and launches a replacement automatically.

16. **Difference between EC2 and ELB health checks?**
* EC2 checks instance status; ELB checks application health.

17. **How does Auto Scaling improve high availability?**
* By replacing failed instances and spreading instances across AZs.

18. **Why integrate Auto Scaling with a Load Balancer?**
* To distribute traffic evenly across dynamically scaling instances.

19. **Which AWS service provides metrics for Auto Scaling?**
* Amazon CloudWatch.

20. **Is Auto Scaling reactive or proactive?**
* Primarily reactive, based on real-time metrics.

21. **Can Auto Scaling work across multiple Availability Zones?**
* Yes, it automatically distributes instances across AZs.

22. **Does Auto Scaling reduce AWS costs?**
* Yes, by terminating unused instances during low demand.

23. **What kind of applications benefit most from Auto Scaling?**
* Applications with variable or unpredictable traffic.

24. **Can Auto Scaling replace unhealthy instances automatically?**
* Yes, it provides self-healing infrastructure.

25. **Is Auto Scaling an AWS certification topic?**
*Yes, it’s a core concept in all EC2-focused certifications.

---

Alright.
This is **file-wise**, **minimum 20 questions per file**, **answers limited to 2–3 lines**, **theory strictly aligned with standard AWS notes**, **no practical steps**, **no fluff**.

I’ll separate clearly so you can revise cleanly.

---

# **DAY 9 – AWS AUTO SCALING (20 Q&A)**

1. **What is AWS Auto Scaling?**
*  A service that automatically adjusts EC2 capacity to meet workload demand and maintain availability.

2. **What problem does Auto Scaling solve?**
*  It prevents over-provisioning during low load and under-provisioning during traffic spikes.

3. **What is an Auto Scaling Group (ASG)?**
*  A logical group of EC2 instances managed together with scaling and health rules.

4. **What is minimum capacity in ASG?**
*  The lowest number of instances the group can run.

5. **What is desired capacity?**
*  The number of instances Auto Scaling tries to maintain at any time.

6. **What is maximum capacity?**
*  The upper limit of instances the ASG can scale to.

7. **What is scale-out?**
*  Automatically adding instances when demand increases.

8. **What is scale-in?**
*  Automatically removing instances when demand decreases.

9. **What triggers Auto Scaling actions?**
*  CloudWatch metrics such as CPU utilization, network traffic, or custom metrics.

10. **What is a Launch Template?**
*   A blueprint defining how EC2 instances are launched, including AMI and instance type.

11. **Difference between Launch Template and Launch Configuration?**
*   Launch Templates support versioning and advanced features; Launch Configurations do not.

12. **What is Target Tracking scaling?**
*   Maintains a metric at a specified target value automatically.

13. **What is Step Scaling?**
*   Scales capacity based on how much a metric exceeds a threshold.

14. **What is Simple Scaling?**
*   Legacy scaling using alarms and cooldown periods.

15. **What is Auto Healing?**
*   Automatic replacement of unhealthy instances in an ASG.

16. **How does Auto Scaling improve availability?**
*   By spreading instances across multiple Availability Zones.

17. **Can ASG work with Load Balancer?**
*   Yes, it integrates with ALB/ELB for traffic distribution and health checks.

18. **What type of applications fit Auto Scaling best?**
*   Stateless and variable-traffic applications.

19. **Is Auto Scaling reactive or proactive?**
*   Primarily reactive, though predictive scaling is available.

20. **What AWS service monitors Auto Scaling metrics?**
*   Amazon CloudWatch.

---

# **DAY 10 – AWS IAM (20 Q&A)**

1. **What is IAM?**
*  A service used to manage access to AWS resources securely.

2. **Is IAM regional or global?**
*  IAM is a global service.

3. **What is an IAM user?**
*  An identity representing a person or application.

4. **What is an IAM group?**
*  A collection of users with shared permissions.

5. **Can groups be nested?**
*  No, IAM groups cannot contain other groups.

6. **What is an IAM role?**
*  An identity with temporary credentials that can be assumed.

7. **Why are IAM roles preferred over access keys?**
*  They use temporary credentials and reduce security risk.

8. **What is an IAM policy?**
*  A JSON document that defines permissions.

9. **What are the main elements of a policy?**
*  Effect, Action, Resource, and optional Condition.

10. **What types of IAM policies exist?**
*   AWS managed, customer managed, and inline policies.

11. **What is least privilege principle?**
*   Granting only the minimum permissions required.

12. **What happens if no policy allows an action?**
*   Access is denied by default.

13. **What takes priority: Allow or Deny?**
*   Explicit deny always overrides allow.

14. **What is MFA in IAM?**
*   Multi-Factor Authentication adds an extra security layer.

15. **What are access keys used for?**
*   Programmatic access via CLI, SDK, or APIs.

16. **Can IAM control application-level users?**
*   No, it only controls AWS resource access.

17. **What is IAM federation?**
*   Allowing external users to access AWS using existing credentials.

18. **Can services assume IAM roles?**
*   Yes, AWS services like EC2 and Lambda can assume roles.

19. **What is credential rotation?**
*   Regularly updating access keys for security.

20. **Does IAM store passwords in plain text?**
*   No, passwords are securely hashed.

---

# **DAY 11 – AMAZON CLOUDWATCH (20 Q&A)**

1. **What is CloudWatch?**
*  AWS service for monitoring, logging, and observability.

2. **What does CloudWatch monitor?**
*  AWS resources, applications, and operational metrics.

3. **What is a CloudWatch metric?**
*  A time-based numerical measurement of resource performance.

4. **What is a namespace in CloudWatch?**
*  A container for related metrics.

5. **What are dimensions?**
*  Key-value pairs that uniquely identify a metric.

6. **What is CloudWatch Logs?**
*  A service for collecting and storing log data.

7. **What is a CloudWatch alarm?**
*  Triggers actions when metrics exceed thresholds.

8. **What actions can alarms trigger?**
*  Notifications, Auto Scaling actions, or automation.

9. **What is CloudWatch Events/EventBridge?**
*  Responds to state changes and enables event-driven workflows.

10. **Does CloudWatch store logs forever by default?**
*   No, log retention must be configured.

11. **Can CloudWatch monitor custom metrics?**
*   Yes, applications can publish custom metrics.

12. **What is a CloudWatch dashboard?**
*   A visual representation of metrics and alarms.

13. **What AWS services use CloudWatch?**
*   EC2, RDS, Lambda, Auto Scaling, ELB, and more.

14. **What metric is most commonly used for Auto Scaling?**
*   CPU utilization.

15. **Is CloudWatch regional or global?**
*   Primarily regional.

16. **What is near-real-time monitoring?**
*   Metrics are updated at short intervals.

17. **Can CloudWatch help in troubleshooting?**
*   Yes, via logs, metrics, and alarms.

18. **What is log group?**
*   A collection of log streams.

19. **What is log stream?**
*   A sequence of log events from a source.

20. **Is CloudWatch used for cost monitoring?**
*   Indirectly, by monitoring usage metrics.

---

# **DAY 12 – AMAZON S3 (20 Q&A)**

1. **What is Amazon S3?**
*  An object storage service with high durability and scalability.

2. **What is stored in S3?**
*  Objects consisting of data, metadata, and a key.

3. **What is a bucket?**
*  A container that stores objects in S3.

4. **Is S3 regional?**
*  Buckets are created in specific regions.

5. **What is object key?**
*  The unique identifier of an object in a bucket.

6. **What durability does S3 provide?**
*  99.999999999% durability.

7. **What is versioning in S3?**
*  Maintains multiple versions of an object.

8. **What are S3 storage classes?**
*  Different tiers optimized for access patterns and cost.

9. **What is lifecycle management?**
*  Automatically transitions or deletes objects.

10. **What is S3 replication?**
*   Copying objects to another bucket or region.

11. **What is S3 bucket policy?**
*   A resource-based policy controlling access.

12. **What encryption options does S3 support?**
*   Server-side and client-side encryption.

13. **What protocol does S3 use for secure access?**
*   HTTPS.

14. **Can S3 host static websites?**
*   Yes, it supports static website hosting.

15. **Is S3 suitable for databases?**
*   No, it is object storage, not relational.

16. **What is eventual consistency?**
*   S3 ensures strong consistency for modern operations.

17. **What are ACLs in S3?**
*   Legacy access control mechanisms.

18. **Is S3 publicly accessible by default?**
*   No, buckets are private by default.

19. **What is S3 used for commonly?**
*   Backups, media, logs, static content, data lakes.

20. **Does S3 support unlimited storage?**
*   Yes, storage is virtually unlimited.

---

# **DAY 13 – AMAZON RDS (20 Q&A)**

1. **What is Amazon RDS?**
*  A managed relational database service.

2. **What type of data does RDS store?**
*  Structured relational data.

3. **Which database engines does RDS support?**
*  MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Aurora.

4. **What does “managed” mean in RDS?**
*  AWS handles backups, patching, and maintenance.

5. **What is Multi-AZ deployment?**
*  A standby replica in another AZ for high availability.

6. **Is Multi-AZ synchronous or asynchronous?**
*  Synchronous replication.

7. **What are Read Replicas used for?**
*  Read scaling and performance improvement.

8. **Are Read Replicas used for failover?**
*  No, mainly for read performance.

9. **What is automatic backup?**
*  Daily snapshots with transaction logs.

10. **What is point-in-time recovery?**
*   Restore database to a specific second.

11. **What is vertical scaling in RDS?**
*   Changing the DB instance size.

12. **What is horizontal scaling in RDS?**
*   Adding read replicas.

13. **How is RDS secured?**
*   VPC isolation, security groups, encryption.

14. **What encryption does RDS support?**
*   Encryption at rest and in transit.

15. **Does RDS support IAM authentication?**
*   Yes, for supported engines.

16. **Is RDS ACID compliant?**
*   Yes, for relational transactions.

17. **Can RDS auto-scale storage?**
*   Yes, storage autoscaling is supported.

18. **What is a DB snapshot?**
*   A manual backup of the database.

19. **Is RDS suitable for analytics?**
*   No, it’s optimized for transactional workloads.

20. **What is Amazon Aurora?**
*   AWS-optimized high-performance relational database.

---

If you want next:

* **MCQs from these**
* **Exam-pattern Q&A**
* **One-page revision version**
* **Comparison tables (IAM vs S3 policies, ASG vs ELB, RDS vs DynamoDB)**

Say exactly what you want next.
