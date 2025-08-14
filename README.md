# CST8919Assignment2 - DevOps Security and Compliance

## Assignment 2 – Cloud Service Alternatives Report

---
## Introduction
This document compares Microsoft Azure security, compliance, and DevSecOps-related services studied in this course with their closest equivalents in Amazon Web Services (AWS) and Google Cloud Platform (GCP).  
Each section provides:
- **Overview** – short description of each service
- **Core Features** – key capabilities and functions
- **Security & Compliance** – relevant certifications and compliance standards
- **Pricing Model** – general cost considerations
- **DevSecOps for DevSecOps** – compatibility with automation, CI/CD, and monitoring tools

---

## Comparison Table

| Azure Service                | AWS Equivalent                         | GCP Equivalent                              |
|------------------------------|----------------------------------------|----------------------------------------------|
| Azure Active Directory (AAD) | AWS IAM + AWS SSO (IAM Identity Center) | Cloud Identity + IAM                         |
| Azure Monitor & Log Analytics| Amazon CloudWatch + CloudTrail + AWS X-Ray | Cloud Monitoring + Cloud Logging + Cloud Trace |
| Azure Policy                 | AWS Config + Service Control Policies  | Organization Policy Service                  |
| Defender for Cloud           | AWS Security Hub + GuardDuty           | Security Command Center + Event Threat Detection |
| Microsoft Sentinel           | Amazon Security Lake + GuardDuty + OpenSearch SIEM | Chronicle Security Operations (SIEM/SOAR)   |

---

## 1. Azure Active Directory (AAD)

### Overview
| Platform  | Service Name | Description |
|-----------|--------------|-------------|
| **Azure** | Azure Active Directory (AAD) | Identity and access management service supporting SSO, MFA, conditional access, and role-based access control. |
| **AWS**   | AWS IAM + AWS SSO (IAM Identity Center) | IAM for fine-grained permissions, SSO for centralized authentication across AWS accounts and apps. |
| **GCP**   | Cloud Identity + IAM | Centralized identity management with SSO, MFA, and granular permissions for Google Cloud resources. |

### Core Features
- SSO & MFA
- Conditional access policies
- Role-based access control (RBAC)
- Integration with on-prem AD
- OAuth 2.0, OpenID Connect, SAML support

### Security & Compliance
- All three support: ISO 27001, SOC 1/2/3, FedRAMP, HIPAA, GDPR

### Pricing Model
- Azure AAD: Free tier, Premium P1/P2 per-user pricing
- AWS IAM: Free; AWS SSO free for AWS services, pay for directory integration
- GCP Cloud Identity: Free and Premium tiers per user

### DevSecOps Integration
- Integrates with CI/CD tools for secure build/deploy pipelines
- Supports API-based identity automation
- Works with secrets managers, policy engines, and cloud-native auth

---

## 2. Azure Monitor & Log Analytics

### Overview
| Platform  | Service Name | Description |
|-----------|--------------|-------------|
| **Azure** | Azure Monitor + Log Analytics | Unified monitoring service with metrics, logs, alerts, and insights. |
| **AWS**   | Amazon CloudWatch + CloudTrail + AWS X-Ray | CloudWatch for metrics/logs, CloudTrail for audit logs, X-Ray for tracing. |
| **GCP**   | Cloud Monitoring + Cloud Logging + Cloud Trace | End-to-end observability platform for metrics, logging, and tracing. |

### Core Features
- Real-time metrics and dashboards
- Log querying & analytics
- Distributed tracing
- Alerts and automation hooks
- Application performance monitoring (APM)

### Security & Compliance
All three support:
- Data encryption in transit and at rest
- Role-based access to logs and dashboards
- Compliance with ISO 27001, SOC, HIPAA, GDPR

### Pricing Model
- Azure: Based on data ingestion & retention, alerts
- AWS: Pay per metric, log ingestion, retention
- GCP: Pay per metric, log ingestion, retention

### DevSecOps Integration
- Connects with CI/CD pipelines for deployment monitoring
- Supports alert-based automation for incident response
- Integrates with security tools for threat detection

---

## 3. Azure Policy

### Overview
| Platform  | Service Name | Description |
|-----------|--------------|-------------|
| **Azure** | Azure Policy | Service for enforcing organizational policies across resources. |
| **AWS**   | AWS Config + Service Control Policies (SCPs) | Config tracks compliance; SCPs enforce governance across accounts. |
| **GCP**   | Organization Policy Service | Applies constraints and governance rules at org/folder/project level. |

### Core Features
- Policy assignment and enforcement
- Compliance auditing
- Custom policy definitions
- Built-in templates for security, cost, compliance

### Security & Compliance
- Enforces security baselines
- Ensures regulatory compliance
- Supports audit logging for governance checks

### Pricing Model
- Azure Policy: No direct cost; charges for compliance scans on some resources
- AWS Config: Pay per configuration item recorded; SCPs free
- GCP Organization Policy: No cost

### DevSecOps Integration
- Integrates into CI/CD for policy-as-code
- Automated deployment validation against governance rules

---

## 4. Microsoft Defender for Cloud

### Overview
| Platform  | Service Name | Description |
|-----------|--------------|-------------|
| **Azure** | Defender for Cloud | Cloud-native security posture management (CSPM) and workload protection (CWPP). |
| **AWS**   | Security Hub + GuardDuty | Security Hub for CSPM; GuardDuty for threat detection. |
| **GCP**   | Security Command Center (SCC) | CSPM, threat detection, and vulnerability scanning. |

### Core Features
- Threat detection and alerts
- Vulnerability scanning
- Compliance score and recommendations
- Multi-cloud security integration

### Security & Compliance
- Meets ISO, SOC, HIPAA, PCI-DSS, GDPR standards
- Supports integration with SIEM tools
- Continuous security posture monitoring

### Pricing Model
- Azure: Free tier (CSPM), paid plans for advanced protection
- AWS: GuardDuty and Security Hub priced per data/event volume
- GCP: SCC Premium billed per asset scanned

### DevSecOps Integration
- Automated remediation workflows
- Security scanning in CI/CD
- API hooks for external SOAR platforms

---

## 5. Microsoft Sentinel

### Overview
| Platform  | Service Name | Description |
|-----------|--------------|-------------|
| **Azure** | Microsoft Sentinel | Cloud-native SIEM/SOAR with advanced threat hunting. |
| **AWS**   | Security Lake + GuardDuty + OpenSearch SIEM | Data lake for security logs, threat detection, and SIEM analytics. |
| **GCP**   | Chronicle Security Operations | SIEM/SOAR platform with Google-scale threat analysis. |

### Core Features
- Centralized log ingestion from multiple sources
- Advanced threat analytics and hunting
- Incident response automation (SOAR)
- Machine learning–based anomaly detection

### Security & Compliance
- Compliance with ISO 27001, SOC, HIPAA, GDPR, FedRAMP
- Supports integration with regulatory log requirements

### Pricing Model
- Azure: Pay per GB of data ingested
- AWS: Security Lake storage costs + GuardDuty data scans + OpenSearch compute
- GCP: Chronicle subscription-based pricing

### DevSecOps Integration
- Connects to CI/CD pipelines for runtime security alerts
- Automated incident response playbooks
- APIs for custom detection rules

---

## Conclusion
Across Azure, AWS, and GCP, equivalent services exist for IAM, monitoring, governance, security posture management, and Sential (SIEM/SOAR).  
Key differences:
- **Azure**: Deep integration between services, strong compliance templates, and policy-as-code capabilities.
- **AWS**: Broadest ecosystem, strong governance at scale via SCPs, powerful threat detection with GuardDuty.
- **GCP**: Simpler integration, strong in analytics and AI-assisted security, competitive pricing on logging/monitoring.

Choosing between platforms depends on:
- Existing cloud investments
- Regulatory/compliance requirements
- DevSecOps workflow maturity
