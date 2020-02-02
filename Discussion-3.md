# What are the different layers of network security on AWS and what unique problems do each solve?
 *In progress*
 
 The AWS network has been architected to permit you to select the level of security
and resiliency appropriate for your workload. To enable you to build geographically
dispersed, fault-tolerant web architectures with cloud resources, AWS has
implemented a world-class network infrastructure that is carefully monitored and
managed.

<H3>Secure Network Architecture</H3>

Network devices, including firewall and other boundary devices, are in place to
monitor and control communications at the external boundary of the network and at
key internal boundaries within the network. These boundary devices employ rule sets,
access control lists (ACL), and configurations to enforce the flow of information to
specific information system services.
ACLs, or traffic flow policies, are established on each managed interface, which
manage and enforce the flow of traffic. ACL policies are approved by Amazon
Information Security. These policies are automatically pushed using AWS’ ACLManage tool, to help ensure these managed interfaces enforce the most up-to-date
ACLs.
Secure Access Points
AWS has strategically placed a limited number of access points to the cloud to allow for
a more comprehensive monitoring of inbound and outbound communications and
network traffic. These customer access points are called API endpoints, and they allow
secure HTTP access (HTTPS), which allows you to establish a secure communication
session with your storage or compute instances within AWS. To support customers
with FIPS cryptographic requirements, the SSL-terminating load balancers in AWS
GovCloud (US) are FIPS 140-2-compliant.
In addition, AWS has implemented network devices that are dedicated to managing
interfacing communications with Internet service providers (ISPs). AWS employs a
redundant connection to more than one communication service at each Internet-facing
edge of the AWS network. These connections each have dedicated network devices.
Transmission Protection
You can connect to an AWS access point via HTTP or HTTPS using Secure Sockets
Layer (SSL), a cryptographic protocol that is designed to protect against eavesdropping,
tampering, and message forgery.
For customers who require additional layers of network security, AWS offers the
Amazon Virtual Private Cloud (VPC), which provides a private subnet within the AWS
cloud, and the ability to use an IPsec Virtual Private Network (VPN) device to provide
an encrypted tunnel between the Amazon VPC and your data center. For more 
Archived
Page 3 of 7
information about VPC configuration options, refer to the Amazon Virtual Private
Cloud (Amazon VPC) Security section below.
Amazon Corporate Segregation
Logically, the AWS Production network is segregated from the Amazon Corporate
network by means of a complex set of network security / segregation devices. AWS
developers and administrators on the corporate network who need to access AWS cloud
components in order to maintain them must explicitly request access through the AWS
ticketing system. All requests are reviewed and approved by the applicable service
owner.
Approved AWS personnel then connect to the AWS network through a bastion host
that restricts access to network devices and other cloud components, logging all activity
for security review. Access to bastion hosts require SSH public- key authentication for
all user accounts on the host. For more information on AWS developer and
administrator logical access, see AWS Access below.
Fault-Tolerant Design
AWS’ infrastructure has a high level of availability and provides you with the capability
to deploy a resilient IT architecture. AWS has designed its systems to tolerate system or
hardware failures with minimal customer impact.
Data centers are built in clusters in various global regions. All data centers are online
and serving customers; no data center is “cold.” In case of failure, automated processes
move customer data traffic away from the affected area. Core applications are deployed
in an N+1 configuration, so that in the event of a data center failure, there is sufficient
capacity to enable traffic to be load-balanced to the remaining sites.
AWS provides you with the flexibility to place instances and store data within multiple
geographic regions as well as across multiple availability zones within each region.
Each availability zone is designed as an independent failure zone. This means that
availability zones are physically separated within a typical metropolitan region and are
located in lower risk flood plains (specific flood zone categorization varies by region).
In addition to utilizing discrete uninterruptable power supply (UPS) and onsite backup
generators, they are each fed via different grids from independent utilities to further
reduce single points of failure. Availability zones are all redundantly connected to
multiple tier-1 transit providers.
You should architect your AWS usage to take advantage of multiple regions and
availability zones. Distributing applications across multiple availability zones provides
the ability to remain resilient in the face of most failure scenarios, including natural
disasters or system failures. However, you should be aware of location-dependent
privacy and compliance requirements, such as the EU Data Privacy Directive. Data is
not replicated between regions unless proactively done so by the customer, thus
allowing customers with these types of data placement and privacy requirements the
ability to establish compliant environments. It should be noted that all 
Archived
Page 4 of 7
communications between regions is across public Internet infrastructure; therefore,
appropriate encryption methods should be used to protect sensitive data.


# What problem do AWS Spot instances solve and how could you use them in your projects?

*In progress*

# Post a screenshot of a lab where you had difficulty with a concept or learned something.

*In progress*
