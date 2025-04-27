# 🚀 Serverless Customer Acquisition Platform for Visa – AWS Free Tier Solution

## 📚 Context
Visa and Ricardo Electro collaborated to grow the Visa customer database through a $1.99 Gillette kit promotion. A real-time test leak led to unexpected traffic surges and exposed signup vulnerabilities.

## 🛠️ Business Challenge
- Massive traffic spike due to early leak.
- Users able to register multiple times via different emails.
- Fraud and resale risk without CPF validation.
- Need for scalable, secure architecture under high demand.

## 🚀 Solution
Designed a serverless AWS architecture to:
- Validate signups with CPF as a unique key.
- Enforce a 1-unit-per-customer limit.
- Handle unexpected traffic via scalable serverless services.
- Engage users post-signup with Pinpoint follow-ups.

## 🖼️ Architecture Diagram
*(Insert your architecture PNG here.)*

## 🏆 Outcomes
- 📈 41% growth in Visa/Mastercard customer database.
- 🔥 300% organic traffic lift for Ricardo Electro over 2 months.
- 🛒 24% e-commerce turnover increase.
- 💵 5x ROAS (Return On Ad Spend).

## 🧰 AWS Services Used

| Service | Purpose |
|:---|:---|
| **Amazon S3** | Static content hosting (registration page) |
| **Amazon CloudFront** | Content Delivery Network (accelerated portal and e-commerce access) |
| **AWS Lambda** | Serverless backend functions (registration, token generation, e-commerce validation) |
| **Amazon API Gateway** | API entry point for secure registration and redirection |
| **Amazon DynamoDB** | Serverless NoSQL database to store CPF and card registration data |
| **AWS WAF** | Web traffic protection and rate limiting |
| **Amazon Cognito** | Optional user authentication management |
| **Amazon CloudWatch** | Monitoring metrics, logs, and alarms |
| **Amazon Pinpoint** | Customer engagement through follow-up messages and notifications |

## 📈 Business Impact
This solution protected the campaign, improved customer activation quality, avoided reselling risks, ensured scalability without infrastructure overhead, and strengthened partnerships with Visa and P&G.

---
