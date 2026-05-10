---
title: Automate General Approval policy process
description: Automate the general approval or rejection of requests based on predefined conditions. Requests are automatically approved when the criteria are met. Otherwise, the system waits for manual approval. You can modify the default policy to include additional conditions as needed.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Review request policies, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Automate General Approval policy process

Automate the general approval or rejection of requests based on predefined conditions. Requests are automatically approved when the criteria are met. Otherwise, the system waits for manual approval. You can modify the default policy to include additional conditions as needed.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## About this task

This procedure demonstrates how to approve or reject an account using the general account approval policy. For example, if an account request includes a predefined approval policy, this process explains how the request is approved or rejected automatically.

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Request Policies**.

2.  Select **Subscription Account Creation General Approval**.

3.  Customize the policy by selecting **Create copy**.

4.  Under the **Policy builder** tab, in the **If** condition block, make a note of the source fields against the highlighted values.

    ![Customizing general approval policy](../image/pace_general_approval.png)

    **Note:** In this section, you’re validating two conditions:

    1.  Business Application = empty
    2.  Application Service = empty
5.  Select **Mappings**.

6.  Verify if the Document assigned is **Automation Activity: General auto approval for subscription account creation**.

    **Note:**

    -   If no document is linked, select **Add** and choose the **General auto approval for subscription account creation** document.
    -   Map only one policy according to automation.
    -   View or create documents in the `sn_itom_cam_automation_activity.list` table.
7.  To remove auto-approval, go to the **Mappings** tab and delete the mapped document.


## What to do next

To test the policy, see [Test updates to a PaCE policy version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-test-policy-version.md).

To publish the policy, see [Publish a PaCE policy version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-publish-policy-version.md).

To add a new approval step in the flow designer, see [Exploring Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-workflow-studio.md).

