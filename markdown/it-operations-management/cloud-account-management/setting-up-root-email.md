---
title: Setting up a root email
description: The app creates accounts with a unique request ID and root email, promoting distinct emails for each account and simplifying management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/cloud-account-management/setting-up-root-email.html
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up AWS cloud, Configuring cloud providers, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Setting up a root email

The app creates accounts with a unique request ID and root email, promoting distinct emails for each account and simplifying management.

Shared root email account benefits:

-   Reduces administrative burden: No need for individual email addresses for AWS accounts.
-   Centralizes notifications: All notifications from the AWS account delivered to a single mailbox.
-   Improves collaboration: Shared email access enables the DevOps team to view and collaborate on tasks.

**Note:** Make sure you note the following points when provisioning a new subscription account:

1.  The app dynamically appends a request ID \(for example, CWSAREQ0000002\) to a predefined root email address \(`aws-ccoe@mycompany.com`\). This process creates a unique email address for each account in a structured format \(`aws-ccoe+CWSAREQ0000002@mycompany.com`\).
2.  After the account is provisioned, AWS sends emails in this format that are received at a central email account `aws-ccoe@mycompany.com`.

-   **[Set up and verify root email in AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/aws-setup.md)**  
Create a unique email address to manage several accounts. Having multiple accounts and emails can be a significant challenge for an AWS admin. A single AD email for multiple AWS accounts simplifies management.

**Parent Topic:**[Setting up AWS cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/setting-up-aws-cloud.md)

