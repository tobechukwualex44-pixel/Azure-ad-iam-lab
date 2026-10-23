# Cloud-Based Active Directory Setup and User Management

## Subtitle
A hands-on IAM lab demonstrating user lifecycle management, dynamic group membership, role-based access control, and offboarding using Microsoft Entra ID.

## Overview
This project simulates how an organization manages identity and access for its HR department in Microsoft Entra ID, Microsoft's cloud-based identity platform. The lab covers the full employee lifecycle from onboarding to offboarding, following the principle of least privilege. It demonstrates how organizations can securely provision users, automate access based on identity attributes, and revoke access when an employee leaves the company.

## Objectives
- Create and manage user accounts in Microsoft Entra ID
- Implement dynamic group membership based on user attributes so users are automatically added to the correct group
- Apply role-based access control, RBAC, following least privilege on a cloud resource group
- Enforce and test multi-factor authentication
- Simulate employee offboarding by disabling account access

## Tools and Technologies
- Microsoft Entra ID, formerly Azure Active Directory, for identity and access management
- Azure resource group as the access-controlled scope, containing a storage account as the target resource representing HR document storage
- Azure role-based access control, IAM, blade
- Entra ID Security Defaults for MFA enforcement

## Step-by-Step Process

### 1. Account and Tenant Setup
This lab begins with a Microsoft Entra tenant and the required Azure subscription configuration. The environment is prepared to support user provisioning, access policies, and cloud resource management.

![Account and tenant setup placeholder] <img width="1470" height="795" alt="Screenshot 2026-10-23 at 4 30 42 AM" src="https://github.com/user-attachments/assets/ade52457-6697-49fc-83d7-a5c56193ba21" />



### 2. Creating Test Users
A set of fictional HR employee accounts is created in Microsoft Entra ID to simulate realistic onboarding scenarios. Each user is assigned identity attributes, such as department, so that group membership can be driven automatically.

![Creating test users placeholder] <img width="1470" height="835" alt="Screenshot 2026-10-23 at 3 51 10 AM" src="https://github.com/user-attachments/assets/c6adde3f-5a8a-44a1-886b-8734861bd567" />


### 3. Creating a Dynamic Security Group
A dynamic security group was configured to automatically assign users based on an HR attribute. The membership rule targets users whose department matches HR, ensuring that individuals are added to the correct access group without manual administration.

![Dynamic security group rule placeholder] <img width="1470" height="799" alt="Screenshot 2026-10-05 at 4 13 40 AM" src="https://github.com/user-attachments/assets/a01c2982-efc3-4e1d-9dab-80e4a1ae3de6" />


### 4. Creating a Target Resource Group
A resource group named "HRO resources OT" was created to represent the HR department's cloud resources, and a storage account was placed inside it to represent HR document storage. Access is controlled at the resource group scope so that only authorized groups can view its contents.

![Resource group and storage account placeholder] <img width="1255" height="836" alt="Screenshot 2026-10-05 at 4 54 57 AM" src="https://github.com/user-attachments/assets/a14fd102-f8c1-43bc-bc26-2b6e50a92c6a" />


### 5. Assigning Role-Based Access Control
The Reader role was assigned to the HR security group on the resource group, following the principle of least privilege. This allowed the group to view resources without being able to change them, and the permission flows down to everything inside the resource group. Eligible versus active assignments and permanent versus time-bound assignment options were also reviewed to illustrate identity governance and privileged access principles.

![Role assignment placeholder]<img width="1259" height="833" alt="Screenshot 2026-10-05 at 6 12 37 AM" src="https://github.com/user-attachments/assets/d8026904-9e8e-42ab-b681-48b864d5a5cb" />

### 6. Testing User Sign-In and MFA Enforcement
A test user login was completed to verify that Security Defaults enforced multi-factor authentication. This validation confirms that a user must complete MFA before being granted access, adding a second layer of identity verification.

![MFA prompt placeholder] <img width="1470" height="802" alt="Screenshot 2026-10-23 at 4 24 00 AM" src="https://github.com/user-attachments/assets/fa096eb7-344c-4d6b-a2df-dfd5579d8599" />

### 7. Simulating Offboarding
An employee account was disabled using the Account Enabled setting during a simulated offboarding event. A follow-up sign-in attempt was blocked, confirming that access revocation was effective and that the account could no longer authenticate to the cloud environment.

![Offboarding blocked placeholder] <img width="1470" height="925" alt="Screenshot 2026-10-05 at 6 50 21 AM" src="https://github.com/user-attachments/assets/5d3621e3-7fcb-4a88-b0ce-5ea67e81a0b3" />


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

