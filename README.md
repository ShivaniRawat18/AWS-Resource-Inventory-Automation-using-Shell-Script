# AWS Resource Inventory Automation Script

A shell script to automate the process of listing **active AWS resources** across different services such as EC2, S3, RDS, Lambda, VPC, CloudWatch, etc.

This script helps DevOps engineers, cloud administrators, and auditors quickly fetch cloud inventory for monitoring, cost savings, or reporting purposes.

---

## 🚀 Features

- Lists active resources for 14+ AWS services:
  - EC2  
  - RDS  
  - S3  
  - CloudFront  
  - VPC  
  - IAM  
  - Route53  
  - CloudWatch  
  - CloudFormation  
  - Lambda  
  - SNS  
  - SQS  
  - DynamoDB  
  - EBS  

- Validates AWS CLI installation & configuration  
- Simple usage with region + service  
- **Cron job automation support**  
- Designed for beginners and DevOps freshers  
- Clean, readable, production-style script  

---

## 📦 Requirements

- AWS CLI installed  
- AWS credentials configured (`aws configure`)  
- Executable permission for the script:  
  ```bash
  chmod +x aws_resource_list.sh
  ```

---

## 🧩 Usage

### **1. List resources for a specific service**
```
./aws_resource_list.sh <aws_region> <service>
```

#### Example:
```
./aws_resource_list.sh us-east-1 ec2
```

---

## ⏱️ Automate with Cron (New Feature)

You can automate daily AWS resource reporting by scheduling the script using:

```
./aws_resource_list.sh --schedule "0 9 * * *" us-east-1 ec2
```

This will automatically:

- Add a cron job  
- Run daily at 9 AM  
- Log output to:  
  ```
  /var/log/aws-inventory.log
  ```

---

## 📁 Supported Services

| Service       | CLI Command Used |
|---------------|------------------|
| EC2           | describe-instances |
| RDS           | describe-db-instances |
| S3            | list-buckets |
| CloudFront    | list-distributions |
| VPC           | describe-vpcs |
| IAM           | list-users |
| Route53       | list-hosted-zones |
| CloudWatch    | describe-alarms |
| CloudFormation| describe-stacks |
| Lambda        | list-functions |
| SNS           | list-topics |
| SQS           | list-queues |
| DynamoDB      | list-tables |
| EBS           | describe-volumes |

---

## 📜 Cron Log File

All automated runs will be saved into:

```
/var/log/aws-inventory.log
```

---

## 👩‍💻 Author

**Shivani Rawat**  
DevOps | Cloud | Automation | AWS | Linux  
(You can add LinkedIn/GitHub links here)

---

## 📝 License
This project is open-source. You may modify or distribute it freely.
