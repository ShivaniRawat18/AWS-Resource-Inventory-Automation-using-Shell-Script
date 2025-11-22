# 🚀 AWS Resource Inventory Automation Script

A production-style **shell script** that automatically lists **active AWS resources** across multiple AWS services such as EC2, S3, RDS, CloudFront, Lambda, VPC, IAM, and more.

This is an excellent project for **DevOps freshers**, showcasing your skills in:

* AWS CLI
* Bash scripting
* Automation
* Logging
* Cron scheduling

---

## ⭐ Features

* Lists active resources for **14+ AWS services**

  * EC2
  * RDS
  * S3
  * CloudFront
  * VPC
  * IAM
  * Route53
  * CloudWatch
  * CloudFormation
  * Lambda
  * SNS
  * SQS
  * DynamoDB
  * EBS

* Validates AWS CLI installation & configuration

* Dynamic usage: provide **region + service**

* **Cron job automation** for scheduled inventory reports

* Saves logs automatically

* Beginner friendly but professional

---

## 📌 Requirements

* AWS account
* AWS CLI installed
* AWS CLI configured (`aws configure`)
* Shell script execution permissions

---

## 🧩 Installation & Setup

### **1. Update package list**

```bash
sudo apt update
```

### **2. Install AWS CLI**

```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

### **3. Configure AWS CLI**

```bash
aws configure
```

Enter:

* AWS Access Key
* AWS Secret Key
* Default region
* Output format (json/text/table)

### **4. Give execute permission to the script**

```bash
chmod +x aws_resource_list.sh
```

---

## ▶️ Usage

### **1. List resources for a specific service**

```bash
./aws_resource_list.sh <aws_region> <service>
```

#### Example:

```bash
./aws_resource_list.sh ap-south-1 ec2
```

---

## ⏱️ Schedule Automatic AWS Inventory Reports

Use cron scheduling like this:

```bash
./aws_resource_list.sh --schedule "*/2 * * * *" ap-south-1 ec2
```

### ✔ Explanation:

* `*/2 * * * *` → runs every 2 minutes
* Fetches EC2 inventory
* Saves output to:

  ```
  /var/log/aws-inventory.log
  ```

---

## 📁 Supported Services

| Service        | CLI Command Used      |
| -------------- | --------------------- |
| EC2            | describe-instances    |
| RDS            | describe-db-instances |
| S3             | list-buckets          |
| CloudFront     | list-distributions    |
| VPC            | describe-vpcs         |
| IAM            | list-users            |
| Route53        | list-hosted-zones     |
| CloudWatch     | describe-alarms       |
| CloudFormation | describe-stacks       |
| Lambda         | list-functions        |
| SNS            | list-topics           |
| SQS            | list-queues           |
| DynamoDB       | list-tables           |
| EBS            | describe-volumes      |

---

## 📝 Cron Log File Location

Logs for automated executions (cron) will be saved to:

```
/var/log/aws-inventory.log
```

---

## 👩‍💻 Author

**Shivani Rawat**
DevOps | AWS | Automation | Linux
(Add your GitHub/LinkedIn links here)

---

## 📜 License

This project is open-source. You may modify or distribute it freely.

---
