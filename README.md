# AWS Security Checklist

This repository provides a **practical AWS Security best practices checklist**.  
It is designed as a reference for common guardrails and security controls in AWS environments.

> For educational and demo purposes only — not a substitute for a full security program.

---

## ✅ Identity & Access Management (IAM)
- [ ] MFA enforced for all IAM users
- [ ] No root account usage (enforce via SCPs or alerts)
- [ ] IAM roles used instead of long-term keys
- [ ] Least privilege policies applied
- [ ] Regular credential rotation and key audits
- [ ] Service Control Policies (SCPs) applied for org-wide guardrails

---

## 🔒 Data Protection
- [ ] S3 buckets private by default
- [ ] Default encryption enabled for all new S3 buckets
- [ ] Encryption at rest enabled (KMS or SSE-S3)
- [ ] Encryption in transit enforced (TLS/SSL)
- [ ] KMS key rotation enabled
- [ ] Secrets stored in AWS Secrets Manager or SSM Parameter Store

---

## 📊 Monitoring & Logging
- [ ] Organization-wide CloudTrail enabled in **all regions**
- [ ] CloudTrail log file validation enabled
- [ ] Logs stored in private, encrypted S3 bucket
- [ ] AWS Config enabled in all accounts/regions
- [ ] VPC Flow Logs enabled
- [ ] Centralized log storage with restricted access

---

## 🌐 Network Security
- [ ] Security Groups follow least privilege
- [ ] NACLs used for subnet-level controls
- [ ] WAF and/or AWS Shield applied to internet-facing apps
- [ ] No unrestricted 0.0.0.0/0 rules (except where justified)
- [ ] Bastion hosts or SSM Session Manager used instead of direct SSH

---

## 🚨 Threat Detection & Response
- [ ] GuardDuty enabled in all accounts/regions
- [ ] Security Hub enabled with **CIS AWS Foundations** and **AWS Foundational Security Best Practices**
- [ ] EventBridge rules forward high-severity alerts to SNS/ChatOps
- [ ] Incident response runbook documented and tested
- [ ] Automated remediation playbooks for common findings

---

## ⚠️ Disclaimer
This checklist is for **educational and awareness purposes**.  
Always tailor controls to your organization’s compliance, workload, and risk profile.
