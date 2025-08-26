# 🚀 Disaster Recovery in AWS using CRR & EFS

## 📌 Project Overview
This project demonstrates how to implement a *Disaster Recovery (DR) solution on AWS* using:
- *Amazon S3 Cross-Region Replication (CRR)*  
- *Amazon Elastic File System (EFS)*  

The solution ensures *business continuity, data integrity, and high availability* by replicating storage resources across AWS regions.

---

## 🛠 Technologies & Services Used
- *Amazon S3* – Object storage with CRR  
- *Amazon EFS* – Managed elastic file storage  
- *Amazon EC2* – Compute resources for testing workloads  
- *Amazon VPC* – Isolated networking environment  
- *AWS IAM* – Identity & Access Management roles and policies  
- *AWS Management Console / CLI* – Setup and configuration  

---

## 📂 Architecture
![Final Architecture](images/architecture.png)

---

## ⚙ Implementation Steps

### 🔹 Step 1: S3 Bucket Setup
- Create a *source bucket* in the Mumbai region.  
- Create a *destination bucket* in Northern Virginia.  
- Enable *versioning* on both buckets.  
- Apply *CRR replication rule*.  

![S3 Bucket Creation](images/s3-bucket.png)

---

### 🔹 Step 2: Apply CRR
- Configure Cross-Region Replication between buckets.  
- Verify that uploaded files are replicated automatically.  

![CRR Rule](images/crr-rule.png)

---

### 🔹 Step 3: EFS Setup
- Create an *Elastic File System (EFS)*.  
- Mount it to an EC2 instance.  
- Enable replication for disaster recovery.  

![EFS Setup](images/efs-setup.png)

---

### 🔹 Step 4: IAM Role
- Create and attach an *IAM Role* with S3 + EFS access policies.  
- Attach role to the EC2 instance to allow secure access.  

![IAM Role](images/iam-role.png)

---

## 📊 Results / Outcomes
- ✅ Data uploaded in *Mumbai S3 bucket* replicated automatically to *Northern Virginia*.  
- ✅ EFS replication ensured *data durability* across regions.  
- ✅ Successful failover testing confirmed *business continuity*.  

---

## 📖 Documentation
The complete *project documentation & report* is included:  
- Disaster recovery in aws using CRR&EFS2.pptx  

---

## 🚀 Future Improvements
- Automate DR setup using *Terraform / CloudFormation*.  
- Add *AWS Lambda* for replication monitoring.  
- Integrate with *AWS Backup* for centralized backup.  

---

## 👨‍💻 Authors
- *Vemana Ajay Babu*  
- *Tanukonda Sai Kalyan*  
- *Sirapu Sai*  

Under the guidance of *Mr. Aashu Dev (AWS Solution Architect, AWS Academy Accredited Educator)*  

---
