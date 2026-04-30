---
title: Identify loss scenarios and align them to the plan
description: When you create a continuity plan or a recovery plan for a department or a business unit, it is necessary to identify and align loss scenarios to the plan.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Identify loss scenarios and align them to the plan

When you create a continuity plan or a recovery plan for a department or a business unit, it is necessary to identify and align loss scenarios to the plan.

## Before you begin

Role required: sn\_bcm.program\_manager

## About this task

As a plan owner identification of loss scenarios helps you to be prepared for any sudden disruptive event and continue with business functions as usual.

When you create a plan using a plan template, the loss scenarios that are identified in the plan template automatically get associated to the plan that you created. Your plan has a basic set of loss scenarios attached to it. You can then add additional loss scenarios to the plan as per your requirement.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click **In Draft** state in the Planning list.

4.  Click the link to the plan record in the **Name** column.

5.  Click the **Loss Scenarios** tab of the plan that opens.

    Use this tab to plan for every disruptive scenario that you can predict, and to manage response and recovery in such a situation.

6.  Click **Add** to add additional loss scenarios to the plan.

7.  Select the scenario names from the Add Loss Scenarios modal form.

8.  Click **Add**.

    The loss scenario is associated to the plan. The Plan Loss Scenario table \[sn\_bcp\_plan\_loss\_scenario\] stores the relationship between the plan and the loss scenario.

9.  To add related asset dependencies to the loss scenario of the plan, click the link to the loss scenario record in the **Name** column.

10. Click **Add** in the Related Asset Dependencies related list to add dependent items.

    1.  To filter items from all the records of the underlying element definition, click the **From all records** button.

        If the loss scenario is loss of business applications, then all impacted applications are filtered and listed.

    2.  Click **Next**.

    3.  Select items from the Add items pop-up.

    4.  Click **Add**.

    1.  To filter items that depend on the plan scope, which is attached to the BIA, click **Based on plan scope**.

    2.  Select the plan scope from the list.

    3.  Click **Next**.

    4.  Select the dependencies of the selected plan scope item attached to the BIA.

    5.  Click **Add**.


**Parent Topic:**[Structured workflows for Business Continuity Planning](../concept/business-continuity-planning-overview.md)

