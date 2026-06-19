---
title: Review request policies
description: Review and update request policies to confirm they align with your cloud account request process. These policies enforce data checks and conditions, promoting consistency in creating cloud subscription accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/viewing-pace-policy.html
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Review request policies

Review and update request policies to confirm they align with your cloud account request process. These policies enforce data checks and conditions, promoting consistency in creating cloud subscription accounts.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## About this task

Certain steps in request processing often require manual intervention. These interventions include general approval, finance approval, and assigning configuration and AWS organizational unit. However, these steps can be automated when specific criteria are met. Cloud Account Management integrates with the PaCE plugin to define and manage these criteria as policies.

For each step, an entry is created in the **sn\_itom\_cam\_automation\_activity** table, and the associated policies are displayed under the **Request Policies** tab in the Cloud Workspace. Each policy is linked to an activity via the **Mappings** tab within the policy, although only one policy is supported according to automation activity.

**Note:** Currently, Azure account creation can’t be automated.

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Request Policies**.

    The existing policies appear under the **All Policies** section and are further classified as active policies and inactive policies.

2.  View or customize an existing policy by selecting the policy name.

3.  Under the **Policy Builder** tab, review the policy conditions.

4.  To modify an existing policy, select **Create copy**.

5.  To add a condition, select **New condition set**.

6.  To remove a condition, select the delete icon \[Omitted image "delete-input-icon.png"\] Alt text: Delete.

    **Note:** For more information on managing policies, see .


## What to do next

These sections explain how to modify, test, and publish the automation policy.

-   [Automate General Approval policy process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-account-management/automate-account-creation-approval.md)
-   [Automate Budget Approval policy process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-account-management/automate-account-budget-approval.md)
-   [Automate Configuration Assignment policy process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-account-management/automate-account-creation-config-assign.md)

