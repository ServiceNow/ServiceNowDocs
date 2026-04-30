---
title: Modify collected metrics under a child policy
description: Turn off an existing DEX metric for certain configuration item \(CI\) criteria by creating a child policy.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Collecting DEX metrics, DEX administration, Configure, Digital End-User Experience, IT Service Management]
---

# Modify collected metrics under a child policy

Turn off an existing DEX metric for certain configuration item \(CI\) criteria by creating a child policy.

## Before you begin

Role required: sn\_dex\_admin

## About this task

Metric collection on any device is managed using agent policies. Agent policies are downloaded on the devices when the list of metrics is downloaded. The metrics are collected based on the CI filter criteria of the policy, and you can modify which metrics are collected. For example, in one of the policies available with the base system.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the DEX Administration icon \(![](../image/icon-administration.png)\).

3.  In the Device and application configuration section, select **Manage policies** on the Agent policies card.

4.  Select the policy for which you want to create a child policy.

5.  Select **Create Child**.

    A child policy inherits the parent policy configuration.

6.  Modify the parent name and description to indicate which new criteria are added to the child policy.

    **Note:** In the **Publish status** field, the value is set to Draft. After you create and save the policy, the value changes to Ready to publish.

    In the **Hierarchy** field, the value is set to None. If you create a child for the current policy, the value changes to Parent.

7.  Update the criteria for the child policy.

    ![A new child policy form with the Name and a new parameter highlighted](../image/acc-policy-child.png)

8.  Select **Save**.

9.  In the Check Instances related list, select the applicable instance name.

10. In the Check Instance form, navigate to **Related Links** &gt; **Check Parameter**.

11. Select **metrics**.

12. In the **Check Parameter** form, modify metrics as needed.

    ![Check Parameter form with the metrics value being updated](../image/acc-policy-child-metrics.png)

13. Select the **Update** button.

14. Select **Return to Policy**.

15. Select **Publish**.

    The **Publish status** value changes to Queued. When the publishing job runs, the value changes to Published, and the policy becomes active on the agent.


