---
title: Create a business continuity plan from a plan template
description: As a program manager you can create a plan for the respective business units that can be used in times of business disruption. You can use a specific plan template for each plan type to streamline the process of a plan creation.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a business continuity plan from a plan template

As a program manager you can create a plan for the respective business units that can be used in times of business disruption. You can use a specific plan template for each plan type to streamline the process of a plan creation.

## Before you begin

Role required: sn\_bcm.program\_manager, sn\_bcm.planner

## About this task

You can create a plan using a pre-configured plan template that suits your requirement. Using the plan template gives you a standard plan layout automatically adding document sections, loss scenarios, and identifying primary elements that are to be recovered. Plan templates help you to focus on the plan content, its tasks, and the effective implementation of the plan.

Creating a plan helps an organization to identify processes, locations, and assets that must be recovered as a priority when there is a disruption. Selecting a plan type helps to identify the elements for recovery and the time by which it should be done.

As a BCM program manager you can create a plan by clicking the **New** button. When you select a template for the plan, all the related information in the template is copied over to the plan after you submit.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  To create a plan from the Business Continuity Home page, click **Create a Plan**.

3.  To view the list of existing plans in different states and to create a plan record, click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

    1.  Click **In Draft** state in the Planning list.

    2.  Click **New**.

4.  Enter plan details in the Create Plan modal form.

5.  Enter a name for the plan and select a plan template.

    Describe the plan name within 255 characters following a naming convention exclusively for your business teams.

    The details of the referenced template are copied over to the plan. Select the business unit, department, and the plan owner applicable to the plan.

6.  Click **Submit**.

    The plan that you created opens up in the record view. This view displays the details of the plan under the headers **Business Unit**, **Department**, **Plan Owner**, and **State**.

    **Note:**

    The tabs that are available in the Plan view depends on the value that you have selected in the **Plan authoring type** field of the [Configure a business continuity plan template](configure-bcp-template.md) that is used in this plan.

    ![Plan authoring type values](../image/PlanTabAuthoringType.png "Plan authoring type values")

    When you create a plan using a template, the plan documentations associated to the plan template are copied over to the documentation section of the plan that you created.

7.  Review the plan details in the **Overview** tab.

8.  Click the **Details** tab to update the plan details.

9.  To save the plan and update its details later, click **Save**.

10. To save and submit it for review, click **Submit for Review**.

    **Note:** You can submit the plan for review only when it is **In Draft** stage.

    When you submit the plan for review, the plan moves to **In Review** state.

    As a plan owner, you can add details to the plan and move it across different states to get it approved finally.

    **Note:** The **State** field is read only. It indicates the status of the plan. Hence, your action on the plan in the UI takes it through to its approved state.

    -   **In Draft**

        It is the state when your plan is under edit. Add documentation sections to the plan, identify recovery teams and set up recovery tasks for the owners, and submit the plan for review.

        To submit for review, confirm that a BCM Lead is assigned to the plan. Otherwise, you can submit the plan for approval.

        After the plan owner submits the plan for review, the state changes to **In Review**. The state of the plan changes to **Submit for Approval** for the plan owner.

    -   **In Review**

        The plan owner can review, edit, and submit the plan for approval.

    -   **Pending Approval**

        When you click **Submit for Approval**, the plan is set to **Pending Approval** state. The approval configurations, approval levels, and approval rules are evaluated against the plan to determine the approvers. If there are no approval records in the requested state for the plan, then as a BCM program manager you can either **Reject** or **Approve** the plan. The state of the plan and its related tables is read only.

    -   **Returned**

        When the plan is rejected, the state is set to **Returned** state.

    -   **Approved**

        When the plan is approved, it moves to **Approved** state.

        The plan and all its related tabs are read only. Your only option to change the status at this state is to move it to **Archived** state.

    -   **Archived**

        When you archive the plan, it becomes read only. All underlying tables from where the plan retrieves its data to populate in the plan assets, related asset dependencies, recovery strategy, documentation, recovery teams, loss scenarios, and recovery tasks tabs become read only. You cannot edit the information in these tabs anymore.

    **Note:** A scheduled job runs weekly to move the plans that have expired to **Archived** state.

11. To export the plan to different locations and make it available for people to execute the plan in a crisis situation, click **Generate PDF**.

    **Note:** You can generate a PDF if you are a plan contributor \(sn\_bcp.plan\_contributor\) or plan manager \(sn\_bcp.plan\_manager\).

    You can generate a PDF of the plan in all states except **Approved** and **Archived** states. If the plan is approved, then by default a PDF is generated and attached to the plan.

    The plan is exported in its entirety with its summary, recovery teams, loss scenarios, recovery tasks, and an appendix table listing the contact number of every member who is part of the recovery team.


