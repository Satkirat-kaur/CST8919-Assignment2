# ASSIGNMENT 2
# Cloud Service Comparison – Azure vs AWS vs GCP

This document compares key Microsoft Azure services used in our course with their closest equivalents in Amazon Web Services (AWS) and Google Cloud Platform (GCP).  
It includes overviews, core features, security and compliance capabilities, pricing models, and DevSecOps integration notes.

---

## **Quick Reference Comparison Table**

| Azure Service                          | AWS Equivalent                  | GCP Equivalent                  |
|----------------------------------------|----------------------------------|----------------------------------|
| Azure Active Directory (SSO, IAM)      | AWS Identity and Access Management (IAM) + AWS SSO | Google Cloud Identity & Access Management (IAM) |
| Azure Monitor & Log Analytics          | Amazon CloudWatch + AWS X-Ray   | Google Cloud Operations Suite (formerly Stackdriver) |
| Azure Policy                           | AWS Config                      | Google Cloud Organization Policy Service |
| Defender for Cloud                     | AWS Security Hub                | Google Security Command Center (SCC) |
| Azure Sentinel (SIEM/SOAR)             | Amazon Security Lake + AWS Detective + AWS GuardDuty | Chronicle Security Operations (SIEM/SOAR) |

---

## **1. Azure Active Directory (SSO, IAM)**

**AWS Equivalent:** AWS IAM + AWS IAM Identity Center (formerly AWS SSO)  
**GCP Equivalent:** Google Cloud Identity & Access Management (IAM)

### Overview
- **Azure AD:** Cloud-based identity and access management for authentication, SSO, MFA, and access policies.
- **AWS IAM:** Controls access to AWS services/resources with users, groups, roles, and policies.
- **GCP IAM:** Assigns permissions to Google Cloud resources via roles, members, and policies.

### Core Features
- **Azure AD:** SSO to 1000s of SaaS apps, conditional access, MFA, hybrid identity sync.
- **AWS IAM:** Fine-grained permissions, federation, temporary credentials, policy-based control.
- **GCP IAM:** Role-based access, service accounts, policy hierarchy, workload identity federation.

### Security & Compliance
All three meet major standards: ISO 27001, SOC, GDPR, HIPAA, FedRAMP (high), etc.

### Pricing Model
- Azure AD: Free tier + Premium P1/P2 per user/month.
- AWS IAM: Free; charges apply for AWS SSO with certain connectors.
- GCP IAM: No extra cost; included in Google Cloud usage.

### DevSecOps Integration
- Works with Terraform, CI/CD pipelines, and API-based role assignment for automated deployments.

---

## **2. Azure Monitor & Log Analytics**

**AWS Equivalent:** Amazon CloudWatch + AWS X-Ray  
**GCP Equivalent:** Google Cloud Operations Suite

### Overview
- **Azure Monitor:** Collects and analyzes performance/health data from apps and resources.
- **AWS CloudWatch:** Monitors logs, metrics, and events for AWS and hybrid environments.
- **GCP Operations:** Integrated monitoring, logging, and trace analysis for Google Cloud.

### Core Features
- Metrics, logs, and traces collection
- Alerting and dashboards
- Application performance monitoring (APM)
- Integration with other services for incident response

### Security & Compliance
- Supports encryption in transit/at rest, role-based access, and compliance certifications.

### Pricing Model
- Pay-as-you-go based on data ingested, stored, and queried.

### DevSecOps Integration
- Integrates with CI/CD pipelines for automated health checks and deployment validation.

---

## **3. Azure Policy**

**AWS Equivalent:** AWS Config  
**GCP Equivalent:** Google Cloud Organization Policy Service

### Overview
- **Azure Policy:** Defines and enforces rules for resource compliance in Azure.
- **AWS Config:** Tracks and evaluates AWS resource configurations.
- **GCP Org Policy:** Restricts configurations based on organizational rules.

### Core Features
- Policy definition and assignment
- Compliance auditing
- Remediation actions
- Integration with governance frameworks

### Security & Compliance
- Supports CIS benchmarks, ISO, NIST, GDPR compliance checks.

### Pricing Model
- Azure Policy & GCP Org Policy: Included.
- AWS Config: Charges per configuration item and compliance check.

### DevSecOps Integration
- Automates compliance checks during deployment with Terraform, ARM, CloudFormation.

---

## **4. Defender for Cloud**

**AWS Equivalent:** AWS Security Hub  
**GCP Equivalent:** Google Security Command Center (SCC)

### Overview
- **Defender for Cloud:** Cloud-native security posture management + threat protection.
- **AWS Security Hub:** Aggregates security findings from AWS services.
- **GCP SCC:** Security visibility and risk assessment for GCP resources.

### Core Features
- Vulnerability scanning
- Threat detection
- Compliance posture dashboards
- Integration with SIEM/SOAR tools

### Security & Compliance
- Meets global security standards (ISO, SOC, HIPAA, PCI DSS, FedRAMP).

### Pricing Model
- Pay-as-you-go, based on number of resources protected.

### DevSecOps Integration
- Integrates into CI/CD workflows for security gates.

---

## **5. Azure Sentinel (SIEM/SOAR)**

**AWS Equivalent:** Amazon Security Lake + AWS Detective + AWS GuardDuty  
**GCP Equivalent:** Chronicle Security Operations

### Overview
- **Azure Sentinel:** Cloud-native SIEM/SOAR platform for security analytics and automation.
- **AWS Security Lake & Detective:** Aggregate and analyze logs; investigate incidents.
- **GCP Chronicle:** SIEM platform with threat detection, investigation, and response.

### Core Features
- Data ingestion from multiple sources
- Advanced analytics and ML-based threat detection
- Automated incident response (SOAR)
- Integration with threat intelligence feeds

### Security & Compliance
- Compliant with ISO, SOC, HIPAA, PCI, and government frameworks.

### Pricing Model
- Pay-as-you-go based on data ingestion and automation runs.

### DevSecOps Integration
- Hooks into pipelines for automated incident detection and remediation.

---

## **Summary**

This comparison highlights how Azure, AWS, and GCP offer similar capabilities for security, compliance, and DevSecOps, though with differences in **pricing models**, **feature depth**, and **ecosystem integration**.  
Choosing the right one often depends on your existing infrastructure, compliance requirements, and team expertise.
