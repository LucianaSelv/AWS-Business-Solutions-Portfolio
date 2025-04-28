# Serverless Customer Acquisition Platform for Visa

## 🚀 Project Overview
This project demonstrates a serverless architecture designed on **AWS Free Tier** services to scale a promotional campaign for Visa and an E-commerce.

Visa and E-commerce partnered to grow Visa's customer database and drive activation through a $1.99 Gillette kit promotion. During real-time testing, an affiliate leak led to unexpected traffic surges and exposed signup vulnerabilities.

It reimagines a real-world case where a high-profile campaign required a **fraud-resistant**, **secure**, and **scalable** solution to maintain customer data integrity, handle high traffic, and ensure seamless customer engagement.

## 🛠️ Business Challenge

### Before Implementation:
- **High-risk traffic** due to leaked pre-campaign test.
- **Users bypassing purchase limits** by using multiple emails.
- **Absence** of strong identity verification mechanisms.
- **Potential** for legal, financial, and brand reputation risks.
- **Need for scalable, secure architecture** under high demand.

### 🛡️ My Role and Impact
- Identified root vulnerabilities in the customer registration system.
- Led crisis management during the campaign leak, collaborating directly with Visa’s head of marketing.
- Protected the campaign integrity and ensured positive partner relations through proactive communication.
- Designed a **serverless AWS architecture** using Free Tier services.
### Proposed and implemented Solutions:
 - Validate signups with CPF as a unique user identifier.
 - Securely collect sensitive user data (name, email, CPF, card) with account authentication.
 - Enforce a 1-unit-per-customer limit.
 - Handle unexpected traffic via scalable serverless services.
 - Monitor metrics and engage customers post-signup.

### 🏆 After Implementation:
- **41% growth** in Visa/Mastercard customer mailing database.
- **300% organic traffic** in E-commerce’s organic web traffic.
- **24% increase** in e-commerce turnover.
- **5x ROAS** (Return On Ad Spend) achieved.
- **Full fraud prevention** and secure data handling implemented

## 🧰 AWS Services Used
| Service | Purpose |
|:---|:---|
| **Amazon Pinpoint** | Campaign messaging (email/SMS blasts) and follow-up engagement |
| **Amazon CloudWatch** | Monitoring system metrics and engagement tracking |
| **Amazon CloudFront** | Content Delivery Network for portal and e-commerce |
| **AWS WAF** | Web Application Firewall to protect against malicious traffic and rate limiting |
| **Amazon Cognito** | user signup, authentication, and identity management |
| **Amazon S3** | Static content hosting (registration portal assets) |
| **Amazon API Gateway** | API management for secure form submissions and redirection |
| **AWS Lambda** | Serverless compute functions (registration, token generation, e-commerce validation) |
| **Amazon DynamoDB** | Serverless NoSQL database storing CPF and registered card data |

## 🔑 Solution Architecture
The Visa campaign architecture integrates multiple AWS services inside a secure **VPC**, fully leveraging the Free Tier and adhering to AWS Well-Architected principles:

- **Amazon Pinpoint** initiates messaging campaigns to drive users to the Visa Portal for acquisition and manages follow-up for engagement.
- **Amazon CloudFront** accelerates content delivery for the registration portal and the e-commerce site, delivering static assets (HTML/CSS/JS) from **Amazon S3**.
- **AWS WAF** secures the portal against malicious traffic and common web exploits.
- **Amazon Cognito** manages user registration, authentication, and secure collection of CPF, card, and personal data.
- **Amazon API Gateway** exposes backend APIs for secure data submissions, token generation, redirection, and e-commerce integration.
- **AWS Lambda** handles business logic:
  - **Registration Lambda**: Validates CPF and card details during registration.
  - **Token Lambda**: Generates secure, time-limited tokens for redirection.
  - **E-commerce Lambda**: Verifies tokens and enforces the **1-unit-per-customer** purchase limit at checkout.
- **Amazon DynamoDB** stores user records and purchase history for validation.
- **Amazon CloudWatch** captures logs, metrics, and monitors application health.
- Backend services operate privately inside the **AWS VPC**, ensuring secure and isolated communication.
  
## 🏗️ Architecture Diagram
![Architecture Diagram](VISA_campaign_architecture_layers.drawio.svg)

## 📺 **Walkthrough Video**

## 📈 Business Impact
This solution protected the campaign, improved customer activation quality, avoided reselling risks, ensured scalability without infrastructure overhead, and strengthened partnerships with Visa and P&G.

## 💡 Cost Optimization
- Fully serverless: No EC2 management.
- Maximum AWS Free Tier usage during early deployment.
- On-demand scaling minimised fixed operational costs.
  
![AWS](https://img.shields.io/badge/AWS-Free%20Tier-orange)
![Serverless](https://img.shields.io/badge/Architecture-Serverless-brightgreen)
![Project](https://img.shields.io/badge/Project-Real%20Business%20Case-blue)

---
