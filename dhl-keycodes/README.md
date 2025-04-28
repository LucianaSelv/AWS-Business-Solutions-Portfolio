# DHL Keycodes - Optimising Courier Operations with AWS

## 🚀 **Project Overview**
This project tackles manual errors in international shipment documentation, which cause delays, incorrect billing, and customs issues. In global courier operations, lost paperwork and mismanaged documentation lead to customs processing delays and lengthy shipment amendments.

By leveraging **AWS services** to automate document handling and account keycode validation, this solution streamlines operations, reduces human error, and ensures efficient customs processing.

The solution mimics integrating the **Metafour SaaS platform** (courier service provider) and **DHL's system** using **API Gateway** and **Lambda** for customs account keycode validation. Lambda validates keycodes, processes documents, and stores them securely in **S3**.

## 🛠️ **Business Challenge**

### Before Implementation:
- **Manual errors** in shipment documentation caused delays and incorrect billing.
- **Customs clearance mistakes** from missing paperwork and incorrect deferment accounts.
- **High amendment rates** to Entry Docs increased operational workload and delays.
- **Flooded inboxes** with frequent customs clearance request emails.
- **Prolonged transit time** averaging 8.7 days per shipment.

### 🛡️ My Role and Impact
- Identified recurring customs processing issues.
- Led the effort with DHL and Metafour to design a keycode validation solution.
- Ensured compliance and process alignment with the UK Customs Clearance team.
- Designed a **serverless AWS architecture** using Free Tier services.
### Proposed and implemented Solutions:
 - Integrate Metafour with DHL’s system for keycode validation via **API Gateway** and **Lambda**.
 - Automate account keycode and document storage securely in **S3**.
 - Enable DHL to adopt the solution for clients with multiple accounts under the same Importer of Record.

### 🏆 After Implementation:
- **78% reduction** in customs clearance request emails.
- Amendment rate dropped to **2%** of total shipments.
- **Transit time** reduced from 8.7 days to 4.3 days.
- Increased **team productivity** and improved **client satisfaction**.


## 🧰 **AWS Services Used**
| **Service**         | **Purpose**                                                            |
|---------------------|------------------------------------------------------------------------|
| **API Gateway**      | Exposes a REST API for keycode validation and document submission       |
| **Lambda**           | Processes keycodes, validates them, triggers automation                 |
| **S3**               | Stores keycodes, commercial invoices, and shipping documents securely with encryption |
| **EventBridge**      | Automates event-driven workflows based on event triggers (keycode entry) |
| **CloudWatch**       | Logs API calls, errors and system performance metrics                       |
| **CloudTrail**       | Provides audit logs for compliance and security tracking      |
| **SQS (DLQ)**        | Dead Letter Queue for handling validation failures      |
| **SNS**              | Sends notifications for critical alerts       |
| **Cognito**          | Manages user authentication for secure API access      |
| **IAM Roles**        | Grants least privilege permissions for Lambda to interact with S3 and other services |

## 🔑 **Solution Architecture**
The architecture integrates multiple AWS services, deployed via AWS CloudFormation, leveraging the Free Tier, and adhering to AWS Well-Architected principles:
- **API Gateway** simulates the Metafour-to-DHL call by receiving HTTP requests from a mock API (simulating Metafour's system), with Cognito handling user authentication.
- **Lambda** (Validator) retrieves keycodes from **S3**, processes and validates them, then uploads documents to an encrypted **S3** bucket. An **IAM Role** with least privilege ensures secure access to resources.
- Validation failures are sent to an **SQS Dead Letter Queue (DLQ)** for error handling.
- **EventBridge** automates any necessary follow-up actions (e.g., notifying a team member or triggering further workflows).
- **CloudTrail** provides audit logs, **CloudWatch Logs** monitors system performance, and **CloudWatch Alarms + SNS** send alerts for issues.

## 🏗️ **Architecture Diagram**
![Architecture Diagram](DHL_Diagram.drawio.svg)
  
## 🛠 **Deployment Approach**

### Prerequisites:
- An **AWS account** (can use the Free Tier)
- **AWS CLI** configured on your machine

### Deployment Method:
The solution was deployed using AWS CloudFormation, enabling infrastructure-as-code for consistency and scalability. The deployment leverages the AWS Free Tier to minimise costs and adheres to the AWS Well-Architected Framework for security, reliability, and operational excellence.

## 📺 **Walkthrough Video**


## 📊 Results & Business Impact

- Faster processing of customs clearance and documents.
- Fewer human errors in deferred account assignments.
- Higher team productivity due to automation.
- Improved client satisfaction with reduced shipment delays.

## 💡 Cost Optimization
- Fully serverless: No EC2 management.
- Maximum AWS Free Tier usage during early deployment.

![AWS](https://img.shields.io/badge/AWS-Free%20Tier-orange)
![Serverless](https://img.shields.io/badge/Architecture-Serverless-brightgreen)
![Project](https://img.shields.io/badge/Project-Real%20Business%20Case-blue)
