---
title: Using Cloud Account Management in Cloud Workspace
description: The Cloud Account Management app in Cloud Workspace manages the lifecycle of your cloud accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/cloud-account-management/using-cam.html
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Using Cloud Account Management in Cloud Workspace

The Cloud Account Management app in Cloud Workspace manages the lifecycle of your cloud accounts.

After setup, day-to-day work involves four tasks: monitoring account status, creating new accounts, managing existing accounts, and certifying accounts.

Start with the dashboards to see which accounts need attention. Create a cloud account to add new accounts, manage accounts and their state. Certify accounts to confirm they remain valid.

## Viewing Cloud Account Management dashboards

The dashboards show the current state of your cloud accounts. The home page reports accounts with critical or high severity, suspended accounts, accounts due for certification, and accounts with undefined budgets. Separate dashboards serve requesters, admins, and compliance users. Identify accounts that need action from the dashboards.

## Creating a cloud account

Request and provision a new cloud account, requests run through the CAM request catalog, and provisioning uses Terraform or the AWS API. Requesters can track their requests on the requester dashboard.

## Managing cloud accounts

Change the state of existing accounts by suspending or reactivating them. You can also add an unmanaged account one created outside the CAM application so that CAM can manage it.

## Certify an account

Certification confirms that an account's details and ownership are still valid. The home page lists accounts that are due for certification.

-   **[Viewing Cloud Account Management dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/about-cam-dashboard.md)**  
Cloud Account Management has two types of dashboards: one for requesters and another for admins. Depending on the logged- in user, an appropriate dashboard appears.
-   **[Creating a cloud account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/creating-an-account.md)**  
Creating a cloud account involves a requester submitting an account request, an approver approving or rejecting the request, and that admin provisioning the account.
-   **[Managing cloud accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/managing-an-account.md)**  
Managing a cloud account enables you to accomplish a range of tasks such as canceling, suspending, or reactivating cloud accounts, and adding unmanaged accounts.
-   **[Certify an account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/certify-account.md)**  
A certification task represents the work of verifying and certifying the data associated with a record. The certifier reviews tasks created after data validation against the published policy. Account certification helps resolve issues like outdated ownership, inactive user profiles, and improper permissions in cloud accounts.

**Parent Topic:**[Cloud Account Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/cam-landing.md)

