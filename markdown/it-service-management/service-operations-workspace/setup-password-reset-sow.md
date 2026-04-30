---
title: Setting up Service Desk assisted Password Reset in Service Operations Workspace
description: The Password Reset application provides a mechanism for end users to either unlock the account or reset their password with the help of service desk support. This feature enables a secure and an efficient password management system. The users must reach out to the service desk agents to update their login credentials.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Setting up Service Desk assisted Password Reset in Service Operations Workspace

The Password Reset application provides a mechanism for end users to either unlock the account or reset their password with the help of service desk support. This feature enables a secure and an efficient password management system. The users must reach out to the service desk agents to update their login credentials.

Before you configure the password reset, you must define the password reset process. For more information, see [Plan your Password Reset processes](https://www.servicenow.com/docs/access?context=t_PlanPasswordReset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

The password reset feature is available in the base system. Alternatively, you can customize the password reset process to meet your organization's needs.

-   **[Assign the Password Reset Service Desk role to the user](../task/assign-sd-role-pr-sow.md)**  
Assign the password reset service desk agent \(password\_reset\_service\_desk\) role to the users to work on the incidents or interactions related to the password reset issues.
-   **[Create credential store for Password Reset in Service Operations Workspace](../task/create-cred-store-pr-sow.md)**  
Create a password reset credential store record to configure access to your credential store server while a user is changing or resetting a password.
-   **[Create password reset process in Service Operations Workspace](../task/create-password-reset-process-sow.md)**  
Create configure credentials, verification methods and settings, and enrollment settings to create a password reset process.
-   **[Configure the verification methods for service desk process in Service Operations Workspace](configuring-verification-methods-pr-sow.md)**  
Create and edit verification methods to ensure they align with service desk processes, and map each verification to a specific process. Upon mapping the processes, integrate them with UXF routes to complete an end-to-end flow for resetting a password in Service Operations Workspace.
-   **[Configure the password policies](../task/configure-password-policies-pr-sow.md)**  
Create a password policy to ensure that all passwords are strong and secure.
-   **[Configure the session properties](../task/configure-session-properties-pr-sow.md)**  
Configure the password reset properties based on the requirement.

**Parent Topic:**[Setting up integrations in Service Operations Workspace for ITSM](setting-up-sow-itsm.md)

