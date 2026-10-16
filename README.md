\# Enterprise AWS Multi-Account Landing Zone \& IAM Security Matrix



\## 🏢 Project Overview

This project establishes a hardened, multi-account enterprise cloud architecture utilizing \*\*AWS Organizations\*\* and a granular \*\*Identity and Access Management (IAM)\*\* infrastructure. The entire environment is built around the \*\*Principle of Least Privilege (PoLP)\*\* and zero-trust security boundaries to protect production data from unauthorized adjustments.



\## 🗺️ Architectural Topology

\*   \*\*Management Account:\*\* Dedicated entirely to consolidated multi-account billing and core governance. No application code runs here.

\*   \*\*Company-Dev-Account:\*\* An isolated sandbox for developers to rapidly build, test, and safely tear down environments.

\*   \*\*Company-Staging-Account:\*\* A pre-production staging floor used to validate application integrity before live releases.

\*   \*\*Company-Prod-Account:\*\* The highly secure production vault hosting live customer-facing web services.



\## 🔐 IAM Identity \& Group Mapping

\*   \*\*Cloud-Admins-Group:\*\* Configured with master `AdministratorAccess` policies \[1.4]. Mapped to `admin-user-01` and `admin-user-02` \[1.4].

\*   \*\*DevOps-Engineers-Group:\*\* Configured with operational `PowerUserAccess` policies to control cloud computing assets. Mapped to `devops-user-01` and `devops-user-02` \[1.4].

\*   \*\*Application-Developers-Group:\*\* Enforces strict least-privilege, granting read/write access solely to `AmazonEC2FullAccess` and `AmazonS3FullAccess` \[1.4]. Mapped to `app-developer-01` \[1.4].



\## ✅ Verification Logs

\*   \[x] Deployed core AWS Organization control plane.

\*   \[x] Provisioned 3 distinct, cryptographically trusted member environments.

\*   \[x] Configured 3 baseline group security access profiles matching corporate guidelines.

\*   \[x] Enforced Zero-Trust principles by creating clean, non-bloated background service identity vectors.

