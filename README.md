# Cloud-Based Active Directory Setup and User Management

## Subtitle
A hands-on IAM lab demonstrating user lifecycle management, dynamic group membership, role-based access control, and offboarding using Microsoft Entra ID.

## Overview
This project simulates how an organization manages identity and access for its HR department in Microsoft Entra ID, Microsoft's cloud-based identity platform. The lab covers the full employee lifecycle from onboarding to offboarding, following the principle of least privilege. It demonstrates how organizations can securely provision users, automate access based on identity attributes, and revoke access when an employee leaves the company.

## Objectives
- Create and manage user accounts in Microsoft Entra ID
- Implement dynamic group membership based on user attributes so users are automatically added to the correct group
- Apply role-based access control, RBAC, following least privilege on a cloud resource
- Enforce and test multi-factor authentication
- Simulate employee offboarding by disabling account access

## Tools and Technologies
- Microsoft Entra ID, formerly Azure Active Directory, for identity and access management
- Azure Storage Account as the test resource representing HR document storage
- Azure role-based access control, IAM, blade
- Microsoft Authenticator for MFA testing

## Step-by-Step Process

### 1. Account and Tenant Setup
This lab begins with a Microsoft Entra tenant and the required Azure subscription configuration. The environment is prepared to support user provisioning, access policies, and cloud resource management.

![Account and tenant setup placeholder](screenshots/account-tenant-setup.png)

### 2. Creating Test Users
A set of fictional HR employee accounts is created in Microsoft Entra ID to simulate realistic onboarding scenarios. Each user is assigned attributes such as department, job role, and location to support later conditional access and dynamic grouping.

![Creating test users placeholder](screenshots/users-list.png)

### 3. Creating a Dynamic Security Group
A dynamic security group was configured to automatically assign users based on an HR attribute. The rule targets users whose department or HR designation matches the relevant group criteria, ensuring that individuals are added to the correct access group without manual administration.

![Dynamic security group rule placeholder](screenshots/dynamic-group-rule.png)

### 4. Creating a Target Resource
An Azure Storage Account was created to represent HR document storage. This resource acts as the test asset where access is controlled and monitored so that only authorized users or groups can read or manage it.

![Storage account placeholder](screenshots/storage-account.png)

### 5. Assigning Role-Based Access Control
The Reader role was assigned to the HR group on the storage account to follow the principle of least privilege. This allowed the group to view the resource without granting unnecessary permissions. Eligible versus active assignments and permanent versus time-bound assignment options were evaluated to illustrate identity governance and privileged access principles.

![Role assignment placeholder](screenshots/role-assignment.png)

### 6. Testing User Sign-In and MFA Enforcement
A test user login was completed to verify that Security Defaults enforced multi-factor authentication. This validation confirms that a user must complete MFA before being granted access, adding a second layer of identity verification.

![MFA prompt placeholder](screenshots/mfa-prompt.png)

### 7. Simulating Offboarding
An employee account was disabled using the Account Enabled setting during a simulated offboarding event. A follow-up sign-in attempt was blocked, confirming that access revocation was effective and that the account could no longer authenticate to the cloud environment.

![Offboarding blocked placeholder](screenshots/offboarding-blocked.png)

## Key GRC and Security Concepts Demonstrated
- Least privilege access control
- Role-based access control, RBAC, versus direct user permissions
- Dynamic group membership for scalable identity governance
- Multi-factor authentication as a security control
- The joiner-mover-leaver user lifecycle
- Separation between eligible and active role assignments as a privileged access management concept

## Skills Demonstrated
- Cloud identity and access management
- Microsoft Entra ID administration
- Access control policy design
- Security testing and validation
- Technical documentation

## Notes
This project was completed independently as self-directed learning, using free-tier Azure and Microsoft Entra ID resources, with fictional test data only.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
