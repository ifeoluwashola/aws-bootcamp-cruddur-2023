# Week 0 — Billing and Architecture
# Destroy your root account credentials, Set MFA, IAM role
I created new AWS account and signed in to the management console then set IAM role and set MFA for the role
# Review all the questions of each pillars in the Well Architected Tool (No specialized lens)
The Well-Architected Tool (WAT) is a framework provided by AWS to help architects and engineers to build the most secure, high-performing, resilient, and efficient infrastructure possible. There are five pillars in the WAT framework, and each one has a set of questions to assess the architecture's overall state. Here are the questions for each pillar:
# Sure, here is a review of all the questions in each of the five pillars in the AWS Well-Architected Tool, without considering any specialized lens:

# 1. Operational Excellence
Operational Excellence is the ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures.
Questions:
How do you manage and automate changes to your infrastructure, application code, and configuration?
How do you capture, aggregate, and analyze logs and metrics?
How do you manage access and authorization to resources?
How do you enable and manage secure access to your resources and data?
How do you plan for and manage disaster recovery and business continuity?
# 2. Security
Security refers to the ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies.
Questions:
How do you protect your data?
How do you manage access and permissions?
How do you protect your network?
How do you protect your compute resources?
How do you protect your information systems?
How do you prepare for security events?
# 3. Reliability
Reliability refers to the ability to prevent, and quickly recover from failures to meet business and customer demand.
Question:
How do you manage change?
How do you test recovery procedures?
How do you handle service outages?
How do you manage cross-region failover?
How do you scale your systems?
How do you automate your processes?
# 4. Performance Efficiency
Performance Efficiency refers to the ability to use computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technologies evolve.
Questions:
How do you select appropriate compute and database resources to meet your performance needs?
How do you monitor resource usage and performance?
How do you analyze and optimize resource utilization?
How do you use caching and content delivery to improve performance?
How do you manage your data to achieve optimal performance?
# 5. Cost Optimization
Cost Optimization refers to the ability to run systems efficiently and to deliver business value at the lowest price point.
Questions:
How do you monitor your costs?
How do you optimize your costs?
How do you choose the right resources for your workload?
How do you evaluate the cost of your system?
How do you manage your data storage costs?
How do you plan for future costs?
# 6. Sustainability
Sustainability refers to the ability to efficiently use computing resources and reduce the environmental impact of your systems.
Questions:
How do you measure and report on the carbon footprint of your systems?
How do you design your systems to minimize the use of resources and energy?
How do you optimize your system to minimize environmental impact?
How do you dispose of hardware and other components in an environmentally responsible manner?
How do you assess and plan for the long-term sustainability of your systems?
# Create an architectural diagram (to the best of your ability) the CI/CD logical pipeline in Lucid Charts
Here is the link to the architectural design:
Cruddur Conceptual Design: https://lucid.app/lucidchart31b8adbb-6266-45cb-8bc9-63402fc1f316/edit?invitationId=inv_1196efe5-e79d-498a-9fe3-2a05607a78b8
Cruddur Logical Design: https://lucid.app/lucidchart/08e16dda-653e-493f-be2b-1158e49772b1/edit?invitationId=inv_6bd247da-64b6-44a5-82cc-bc33c7cb489d

# Research the technical and service limits of specific services and how they could impact the technical path for technical flexibility. 
Each of the services used in the architectural diagram has its own set of technical and service limits that can impact the technical path for technical flexibility. Here's a brief overview of the limits and potential impact for each service:

AWS Cloud: While AWS Cloud offers virtually unlimited scalability, it has a limit on the number of resources that can be created in a given region. This limit can impact the ability to scale quickly in response to increased demand.

EC2: Amazon Elastic Compute Cloud (EC2) is a scalable computing service that allows users to create virtual machines. The main limit for EC2 is the number of instances that can be launched in a region. If this limit is reached, it can impact the ability to scale and meet demand.

Load Balancer: AWS Load Balancer is used to distribute traffic across multiple EC2 instances. The main limit for the load balancer is the number of connections it can handle. If this limit is reached, it can impact the performance of the application.

Route53: Amazon Route 53 is a DNS service that provides reliable and scalable routing of web traffic. The main limit for Route53 is the number of queries per second it can handle. If this limit is reached, it can impact the ability to route traffic effectively.

AWS AppSync: AWS AppSync is a fully managed service that allows developers to build GraphQL APIs by connecting to various data sources. The main limit for AppSync is the number of requests per second it can handle. If this limit is reached, it can impact the performance of the API.

DynamoDB: Amazon DynamoDB is a NoSQL database that is fully managed and provides scalability and performance. The main limit for DynamoDB is the number of read and write requests per second it can handle. If this limit is reached, it can impact the ability to read and write data effectively.

Amazon RDS: Amazon Relational Database Service (RDS) is a fully managed relational database service that provides scalability and high availability. The main limit for RDS is the number of connections it can handle. If this limit is reached, it can impact the performance of the application.

VPC: Amazon Virtual Private Cloud (VPC) is a virtual network that provides a customizable network configuration. The main limit for VPC is the number of subnets that can be created in a region. If this limit is reached, it can impact the ability to create a network configuration that meets specific requirements.

Authentication: Authentication services such as Amazon Cognito or Auth0 can have limits on the number of users that can be authenticated or the number of requests per second that can be handled. If these limits are reached, it can impact the ability to authenticate users effectively.

Frontend (React.js): React.js is a popular frontend library that can be used to build web applications. The main limit for React.js is the performance of the client-side rendering. If the application becomes too complex or the data volume becomes too large, it can impact the performance of the application.

Backend Python (Flask): Flask is a lightweight web framework that can be used to build web applications. The main limit for Flask is the performance of the backend server. If the application becomes too complex or the data volume becomes too large, it can impact the performance of the server.

REST API: REST APIs can have limits on the number of requests per second they can handle. If this limit is reached, it can impact the performance of the API and the ability to serve requests effectively.

Serverless Cache: Serverless cache services such as Amazon ElastiCache can have limits on the number of requests per second they can handle. If this limit is reached, it can impact the ability to serve requests effectively and impact