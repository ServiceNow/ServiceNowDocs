---
title: Setting up a root email
description: The app creates accounts with a unique request ID and root email, promoting distinct emails for each account and simplifying management.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up AWS cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
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

