---
title: Review default Cloud Account Management certification policy
description: Review the default certification policy provided in Cloud Account Management to validate data against the policy set. This default policy certifies all available cloud service accounts every 90 days. Administrators can customize the default policy or create one as needed.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Certification in Cloud Workspace, Certification in CW]
breadcrumb: [Setting up Cloud Account Management in Cloud Workspace, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Review default Cloud Account Management certification policy

Review the default certification policy provided in Cloud Account Management to validate data against the policy set. This default policy certifies all available cloud service accounts every 90 days. Administrators can customize the default policy or create one as needed.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Account Certification**.

    The policies dashboard opens in CMDB Workspace, displaying existing policies under the **Published Policies** section.

2.  Select **CW Certification Policy** &gt; **View Policy** to review policy details.

3.  For creating or customizing a policy, see [Create a CMDB Data Manager policy](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    **Note:**

    -   To stop data validation or edit a policy, select **Deactivate Policy**.
    -   After the policy is executed, view tasks by selecting the **My Work** tab.
    -   Once the tasks are assigned to the Cloud Account Management Certifier group, it enables certifiers to review read-only fields and modify those fields that they’re permitted to edit.
    -   For certifying an account, see [Certify an account](certify-account.md).

## What to do next

[Review request policies](../concept/viewing-pace-policy.md)

