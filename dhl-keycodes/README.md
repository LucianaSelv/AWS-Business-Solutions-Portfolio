# DHL Keycodes - Optimising Courier Operations with AWS

## 🚀 **Project Overview**
This project aims to address manual errors in international shipment documentation, which often cause delays, incorrect billing, and customs clearance problems. In global courier operations, lost paperwork and mismanaged documentation lead to customs delays, billing errors, and lengthy shipment amendments.

By leveraging **AWS services** and automating document handling and keycode validation, this solution streamlines operations, reduces human error, and ensures seamless customs processing.

The solution mimics an integration between the **Metafour SaaS platform** (courier service provider) and **DHL's system** using **API Gateway** and **Lambda** for customs account keycode validation. Lambda validates keycodes, processes documents, and stores them securely in **S3**.

This solution significantly reduces operational inefficiencies and improves customer satisfaction by automating documentation processes.

## 💼 **Business Problem**

### Before Implementation:
- **Manual errors** in international shipment documentation caused delays and incorrect billing.
- **Customs clearance errors** due to incorrect deferment accounts and missing paperwork.
- **Frequent amendments** to Entry Docs caused high operational workload and delays.
- **78% of emails** were customs clearance requests, flooding team inboxes.
- **Transit time** for shipments averaged 8.7 days.

### Solution Implemented:
- **API Gateway** + **Lambda**: Automated document validation and keycode processing.
- **S3**: Secure storage for commercial invoices and shipping documents.
- **DynamoDB**: Validates keycodes against master account records.
- **CloudWatch**: Monitors and tracks API calls, errors, and system performance.
- **EventBridge**: Triggers workflows based on keycode entries for further automation.

### After Implementation:
- **78% reduction** in customs clearance request emails.
- Amendment rate dropped to **2%** of total shipments.
- **Transit time** reduced from 8.7 days to 4.3 days.
- Increased **team productivity** and improved **client satisfaction**.


## 🔧 **AWS Services Used**
| **Service**         | **Purpose**                                                            |
|---------------------|------------------------------------------------------------------------|
| **API Gateway**      | Exposes a REST API for keycode validation and document submission       |
| **Lambda**           | Processes keycodes, validates them, triggers automation                 |
| **S3**               | Stores commercial invoices and shipping documents securely             |
| **EventBridge**      | Automates event-driven workflows based on event triggers (keycode entry) |
| **DynamoDB**         | Stores keycodes for validation                                         |
| **CloudWatch**       | Logs API calls, errors and system performance metrics                       |
| **IAM Roles**        | Grants the necessary permissions for Lambda to interact with S3 and DynamoDB |

## 🔑 **Solution Architecture**
The architecture integrates multiple AWS services:
- **API Gateway** simulates the Metafour-to-DHL call by receiving HTTP requests from a mock API (simulating Metafour's system).
- **Lambda** processes the keycode, validates it using **DynamoDB**, and uploads necessary documents to **S3**.
- **EventBridge** automates any necessary follow-up actions (e.g., notifying a team member or triggering further workflows).
- **S3 Versioning** ensures all documents are versioned, providing traceability and improved error management.

## 🛠 **Deployment Instructions**

### Prerequisites:
- An **AWS account** (can use the Free Tier)
- **Terraform** installed for deploying the infrastructure
- **AWS CLI** configured on your machine

### Step-by-Step Deployment:

## 📊 Results & Business Impact

- Faster processing of customs documents.
- Fewer human errors in deferment account assignments.
- Higher team productivity due to automation.
- Improved client satisfaction with reduced shipment delays.

## 💡 **Future Enhancements**
- Expand integration with additional courier services (FedEx, UPS, etc.).
- Introduce AI-powered anomaly detection for customs clearance risks.
- Implement automated invoice generation linked to keycode validation.
  
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo/dhl-keycodes.git
   cd dhl-keycodes
