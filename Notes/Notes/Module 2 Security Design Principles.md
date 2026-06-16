# Module 2: Security Design Principles

Favorite: No
Archive: No
Notebook: AWS Cloud Security  (../../AWS%20Cloud%20Security%2037a6c6880dca808794ffd649839ae789.md)
Edited: June 10, 2026 10:26 AM
Created: June 10, 2026 9:38 AM

## 1. Apply principle of least privilege

- Grant access as needed
- Enforce separation of duties
- Avoid long-term credentials
    - Only grant access to data and other resources to the people who really need that access.
    - Enforce separation of duties with appropriate authorization for each interaction with your AWS resources.
    - Avoiding long-term credentials can diminish attack surface area, instead use temporary credentials and require identities to dynamically acquire them.
    - In AWS, IAM is the primary service for permissions management. It provides the ability to control user and programmatic access to AWS services and resources.

## 2. Enable traceability

- Monitor actions and changes
- Use logs and metrics
- Audit your cloud resources
    - You can monitor, alert, and audit actions and changes to environment in real time. AWS provides native logging and services that can provide greater visibility in near real time for occurrences in environment.
    - Integrate these tools with existing logging and monitoring solutions. Know what workloads are deployed and operational so that you can audit and ensure that the environment is operating at expected security governance levels and meeting required security standards.
    - Several AWS services can help with traceability; CloudTrail logs, AWS API calls, and Amazon CloudWatch provide monitoring of metrics with alarming, and AWS Config provides configuration history.

## 3. Secure all layers

- Use a Defense in Depth approach
- Use different AWS services
    - Apply security in multiple layers with other security controls, such as applying security to network, application, and data store.
    - Example. You can require users to strongly authenticate to an application, additionally, ensure users come from a trusted network path and require access to the decryption keys to process encrypted data.
    - You can use several AWS services together to provide a secure environment for data and resources.
    - AWS customers are able to tailor or harden the configuration of an EC2 instance, Amazon Elastic Container service, or AWS Elastic Beanstalk instance, and persist this configuration to an immutable Amazon Machine Image (AMI), then all new virtual servers, or instances, launched with this AMI receive the hardened configuration, whether they are launched manually or through automatic scaling.

## 4. Automate Security

- Automate routine security tasks with APIs
- Implement Infrastructure as code
    - AWS develops purpose-built security tools that can help you to automate many of the routine tasks that security experts normally spend time on.
    - You can automate security engineering and operations functions by using a comprehensive set of APIs and tools.
    - You can fully automate identity management, network security, and data protection, and monitoring capabilities, and deliver them by using popular software development methods that you already have in place.
    - In the AWS Cloud, you can also turn your infrastructure into code, you can automate the creation of trusted environments to conduct deeper investigations and forensics, you can run incident response simulations and use tools with automation to increase speed for detection, investigation, and recovery.
    - By automating deployments and maintenance, you can remove operator access to reduce attack surface area.

## 5. Protect data in transit and at rest

- Use encryption and access controls
- Classify data with tags
- Use VPN and TLS connections
    - AWS provides services and features that help to protect data at rest and in transit.
    - Safeguards include fine-grained access controls to objects, creating and controlling the encryption keys that are used to encrypt their data, selecting appropriate encryption methods, integrity validation, and appropriate data retention.
    - Another best practice to help manage protection is implementing a tagging schema to classify your data into sensitivity levels.
    - Construct mechanisms to protect data in transit such as using a VPN and TLS connections

## 6. Prepare for security events

- Mitigate the impact of security incidents
- Create processes to isolate incidents and restore operations
    - Even with mature preventive and detective controls, you should put processes in place to respond to and mitigate the potential impact of security incidents.
    - The architecture of your workload strongly affects your ability to operate effectively during an incident.
    - Isolate or contain systems and restore operations to a known good state. Put tools and access in place ahead of a security incident, then routinely practice incident response through game days.
    - Practices that facilitate effective incident response:
        - Detailed logging. Logs can contain important content such as file access and changes.
        - Automatically process events and invoke tools that automate responses through use of AWS APIs.
        - Pre-provision tooling in a “clean room” by using CloudFormation. This provides ability to carry out forensics in a safe, isolated environment.

## 7. Minimize the attack surface

- Be ready to scale and absorb the attack
- Safeguard exposed resources
    - Reduce exposure to unintended access by hardening operating systems and minimizing the components, libraries, and externally consumable services in use.
    - Start by reducing unused components such as OS packages and applications.
    - Configure security groups and network ACLs in VPC to help reduce the attack surface of your applications.
    - AWS services like AWS Auto Scaling and Amazon CloudFront, help applications to scale to absorb common infrastructure layer attacks such as UDP reflection attacks, SYN floods.
    - By using techniques such as automatic scaling, you can absorb larger volumes of application layer attacks.

## Key takeaways: Security Design Principles

- The design principles for security in the Cloud are:
    - Apply principle of least privilege
    - Enable traceability
    - Secure all layers
    - Automate security
    - Protect data in transit and at rest
    - Prepare for security events
    - Minimize attack surface