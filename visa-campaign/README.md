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

## 🏗️ Architecture Diagram
![Architecture Diagram](VISA_campaign_architecture_layers.drawio.svg)

## 🏆 Outcomes
- 📈 41% growth in Visa/Mastercard customer database.
- 🔥 300% organic traffic lift for Ricardo Electro over 2 months.
- 🛒 24% e-commerce turnover increase.
- 💵 5x ROAS (Return On Ad Spend).



## 📈 Business Impact
This solution protected the campaign, improved customer activation quality, avoided reselling risks, ensured scalability without infrastructure overhead, and strengthened partnerships with Visa and P&G.

---
