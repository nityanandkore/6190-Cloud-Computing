# What are the different layers of network security on AWS and what unique problems do each solve?
 
 The AWS network has been architected to permit you to select the level of security
and resiliency appropriate for your workload. To enable you to build geographically
dispersed, fault-tolerant web architectures with cloud resources, AWS has
implemented a world-class network infrastructure that is carefully monitored and
managed.
<h3>Service-level hardening</h3>
Since Amazon.com uses many AWS services for its internal architectures, it only makes sense that AWS would harden select services, like CDN (via the service “CloudFront”) and Load Balancers (ALB, NLB, ELB for Application, Network, and Elastic Load Balancer) for all customers. In the case of CloudFront and the *LB services, AWS goes as far as to outright block UDP traffic (UDP is the protocol of choice for many DDoS attacks like amplification). Due to the sensitive nature of the data inside, AWS even forces on-the-wire (SSL/TLS) encryption when using services like their archival service, Glacier or their DNS service, Route 53. Glacier, which is used heavily to archive Governance, Regulation and Compliance (GRC) data, also goes one step further by natively encrypting all data at rest. Just by using any of the aforementioned services, one automatically blocks entire vectors of attack.

<h3>Identity and access control</h3>
AWS offers several services to authenticate and control access for both internal (administrators and developers) and external (end-users, customers or partners) users. At the heart of AWS’ access control is their holistic Identity and Access Management (IAM) service. This service allows you to create both long-standing and federated (short-term, expiring) accounts for both types of users, and it can lock down access (for most services) to both the individual API call (like “Start Instance” on EC2) and individual resource (like “instance id i-12345) or resource family (like “t2 family” of EC2). Federated access can be provided via social media network (for external users of, perhaps, a mobile game), Active Directory, or SAML. Mobile access can also be enabled by another service called Cognito which allows you to set up and manage entire fleets of potentially millions of users.

<h3>Native encryption options for select services</h3>
As stated earlier, AWS forces SSL/TLS for some sensitive services like Glacier and Route 53, but for other services where some customers may wish to selectively enable encryption, AWS offers both on-the-wire as well as at-rest encryption capabilities. Some services like EBS (SAN disk you can attach to EC2), S3 (AWS’ object store), and Redshift (AWS’ Data Warehouse) make at-rest encryption as easy as checking a box in a web form. For users requiring the highest level of at-rest encryption possible, AWS offers two key management services—KMS and HSM—which can be used to encrypt data (both natively for select service, and client side for non-native) at rest with user-controlled keys.

<h3>Auditing and logging</h3>
Many services (like S3, Redshift and others) provide the ability to turn on logging to track access and other activity of that individual service, but AWS also has several security-minded platform-wide auditing and logging services you should be aware of:

<h4>CloudTrail:</h4> Wouldn’t it be nice to get detailed information about every API call (both successful and unsuccessful) that was made to your back-end? By turning on CloudTrail (must be turned on in every region you operate), you get exactly that—Apache Commons-type logging info (remote IP, user agent, credentials used, timestamp, etc.) for every single API call that anyone makes to any of the thousands of GA’d features that AWS provides. These logs, in combination with the output of AWS Config, are often all one needs to implement a large part of a GRC-related stack.

<h4>CloudWatch Logs:</h4> CloudWatch Logs provide the ability to consume any log file format (even custom ones only your organization uses), from any source (on-premise or AWS-hosted), and trigger alarms and alerts on the data contained inside. One could use this service to raise both operational (e.g. resource scarcity) and security (e.g. hacking attempt) alerts on any data point coming from any product you use.

<h4>AWS Config and Config Rules:</h4> The first time you point AWS Config at your account, it can do resource discovery and inventory, telling you everything you have deployed in AWS and how it is configured. AWS Config will then run periodically (about every 5-15 minutes) and capture the deltas from the previous config run. One could then hand the AWS Config snapshots to an auditor requesting the configuration of a certain resource on a certain day at a certain time. Config Rules takes this one step further by providing automated issue resolution when, for example, it detects that a disk which should be encrypted isn’t. Config Rules can automatically set that disk back to encrypted without any human intervention.

# What problem do AWS Spot instances solve and how could you use them in your projects?

Spot instances, next to On-demand and Reserved instances are another financial model for your EC2 workloads. With On-demand, you pay a fixed hourly price per instance. With Reserved instances, you’re able to reduce your EC2 cost by around 30-40% in exchange for a 1 or 3 year commitment to AWS. While Reserved instances bring you a significant discount compared to On-demand, you are tied into this commitment. If AWS reduces their prices or introduces new instance types that are cheaper, your savings could end up lower and you’ll still be paying for your Reserved instances until the end of the commitment.

Spot instances work on a supply and demand model, meaning AWS takes advantage of unused instance capacity, giving you the opportunity to save as much as 90% compared to the On-demand cost.

# Post a screenshot of a lab where you had difficulty with a concept or learned something.

I have completed the lab mentioned for this week.
