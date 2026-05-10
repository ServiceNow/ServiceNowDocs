---
title: Automate Configuration Assignment policy process
description: Automate assigning configurations and AWS organizational units in requests based on specified conditions. When conditions are met and approvals are complete, requests move forward without admin input. Update the default policy to include specific conditions and values for configuration and AWS organizational unit.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Review request policies, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Automate Configuration Assignment policy process

Automate assigning configurations and AWS organizational units in requests based on specified conditions. When conditions are met and approvals are complete, requests move forward without admin input. Update the default policy to include specific conditions and values for configuration and AWS organizational unit.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## About this task

This procedure demonstrates how to assign account configuration using the assignment policy. For example, when the account creation request is approved and awaits for the provisioning configuration information, this automation is executed.

![Approved CW request waiting for configuration assignment](../image/cam_config_list.png)

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Request Policies**.

2.  Select **Subscription Account Creation Configuration Assignment**.

3.  Customize the policy by selecting **Create copy**.

4.  Under the **Policy builder** tab, in the **If** condition block, make a note of the values that you're validating.

    ![Customizing Configuration Assignment policy](../image/pace_config.png)

    **Note:** In this section, you're validating:

    1.  Environment = Development
    2.  Business unit = business-app-1
5.  To select the configuration and AWS org unit output, select **Data collectors** from the Data sources section.

6.  Select **Add**.

7.  Select **Get Config Assignment Results**.

8.  In the **Add data collector** pop-up, enter `Label` and `Variable name`.

    These field values are only used to identify the data collector.

    ![Data collector dialog box](../image/add_data_collector1.png)

9.  Under the **Inputs** tab, select **CW Application Configuration** and **CW Account Group** \(same as the AWS org unit that an admin selects on the account request screen\).

    ![Data collector dialog box for inputs tab](../image/add_data_collector2.png)

    **Note:** The selected AWS org unit in the data collector should be part of the same Cloud Organization provided in the configuration.

10. Select **Save**.

    The new data collector entry is saved. Only when the **If** condition is met, the **then** condition get executed.

11. Select the output result as follows.

    ![Then condition result](../image/pace_then_config.png)

12. To save the policy, select **Save**.

    **Note:**

    -   If necessary, you can enhance the Log message for the result. For some examples, you can see the default-published policies.
    -   Map only one policy according to automation.
    -   This configuration approval policy is inactive by default. You can deactivate to stop the automation.

## What to do next

To test the policy, see [Test updates to a PaCE policy version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-test-policy-version.md).

To publish the policy, see [Publish a PaCE policy version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-publish-policy-version.md).

To add a new approval step in the flow designer, see [Exploring Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-workflow-studio.md).

