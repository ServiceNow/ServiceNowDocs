---
title: Establish recovery strategies for asset dependencies
description: Use the Loss Scenarios tab to add asset dependencies and identify recovery strategies to deal with various loss scenarios. A plan, complete with recovery strategies for the identified loss scenarios, helps to address gaps that exist.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Establish recovery strategies for asset dependencies

Use the **Loss Scenarios** tab to add asset dependencies and identify recovery strategies to deal with various loss scenarios. A plan, complete with recovery strategies for the identified loss scenarios, helps to address gaps that exist.

## Before you begin

Role required: sn\_bcm.program\_manager or sn\_bcm.planner

## About this task

As a program manager, you can check if there are recovery strategies for various loss scenarios of the plans owned by the planners. Such assessments enable you to be prepared for those scenarios.

When you see the details of a loss scenario associated to a plan, you can also view the assets that are attached to the plan, and the recovery strategies for each of these assets. For example, NYC datacenter can be a related asset for a datacenter outage loss scenario of a customer support plan. You can create a recovery strategy by estimating the time to implement the strategy to get the NYC datacenter up and running.

![Strategy coverage for a related asset](../image/AssetRecoveryStrategy.png "Strategy coverage for related assets")

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click the **In Draft** state in the Planning list.

4.  Click the link to the plan record in the **Name** column.

5.  Click the **Loss Scenarios** tab of the plan.

6.  Click the link to the loss scenario record in the **Name** column.

7.  To add a related asset to the existing list of assets that can be impacted and dependent on the plan loss scenario, click the **Related Asset Dependencies** tab.

    For more information, see [Identify loss scenarios and align them to a business continuity plan](loss-scenarios-align-with-bcp.md#rel-asset-dependencies).

8.  To remove an asset from the plan, select the item and click **Remove**.

    **Note:** You can add or remove an asset, dependent on the plan, only if you are a program manager or owner of the plan.

9.  To establish a strategy and recover a critical asset, click the **Recovery Strategies** tab.

    1.  Click the **New** button.

    2.  Enter a name and description for the recovery strategy and determine the implementation details to recover the asset.

    3.  Click **Save**.

10. To add a recovery task to the recovery strategy of a plan’s loss scenario, click the **Recovery Tasks** tab.

    You can create a recovery task at the recovery strategy level and also at the plan level. See: [Create, update, and group recovery tasks](bcp-recovery-tasks-grid.md#create-rec-task).


