---
title: Automate Budget Approval policy process
description: Automate finance approvals for Cloud Account Management requests based on predefined conditions. Approve requests automatically when criteria are met. Otherwise, wait for manual approval. Modify the default policy to include additional conditions as necessary.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Review request policies, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Automate Budget Approval policy process

Automate finance approvals for Cloud Account Management requests based on predefined conditions. Approve requests automatically when criteria are met. Otherwise, wait for manual approval. Modify the default policy to include additional conditions as necessary.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## About this task

This procedure demonstrates how to approve or reject a budget using the account budget approval policy. For example, if an account request includes a predefined approval policy, this process explains how the budget request is approved or rejected automatically.

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Request Policies**.

2.  Select **Subscription Account Creation Budget Approval**.

3.  Customize the policy by selecting **Create copy**.

4.  Under the **Policy builder** tab, in the **If** condition block, make a note of the source fields against the highlighted values.

    ![Customizing budget approval policy](../image/pace_budget_approval.png)

    **Note:** In this section, you're validating two conditions:

    1.  Environment = Development
    2.  Monthly budget &lt;= 500
    1.  Environment = Development or Test
    2.  Monthly budget = &gt; 5000
5.  Select **Mappings**.

6.  Verify if the Document is assigned to **Automation Activity: Finance auto approval for subscription account creation**.

    **Note:**

    -   If no document is linked, select **Add** and choose the **Finance auto approval for subscription account creation** document.
    -   Map only one policy according to automation.
    -   View or create documents in the `sn_itom_cam_automation_activity.list` table.
7.  To remove auto-approval, go to the **Mappings** tab and delete the mapped document.


## What to do next

To test the policy, see [Test updates to a PaCE policy version](https://www.servicenow.com/docs/access?context=pace-test-policy-version&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

To publish the policy, see [Publish a PaCE policy version](https://www.servicenow.com/docs/access?context=pace-publish-policy-version&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

To add a new approval step in the flow designer, see [Exploring Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

