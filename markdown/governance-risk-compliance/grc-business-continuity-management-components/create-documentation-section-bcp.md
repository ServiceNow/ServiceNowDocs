---
title: Create documentation sections
description: Create a documentation section in the business continuity plan. You can then document the recovery capabilities of your business continuity plan in BCM UIB Workspace.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create documentation sections

Create a documentation section in the business continuity plan. You can then document the recovery capabilities of your business continuity plan in BCM UIB Workspace.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

These UI actions are available for the documentation sections:

-   **Update**: Update an existing documentation section.
-   **Delete**: Delete an existing documentation section.
-   **Reset to template**: Reset an existing documentation section to the Documentation Sections template. You can view the available templates by navigating to **Documentation Sections** of **Business Continuity** in the application navigator. For an existing documentation section, the **Update**, **Delete**, and **Reset to template** actions are available. For a new documentation section, the **Reset to template** action is not available.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Planning** and select the link to the plan record in the **Name** column.

3.  Select the **Documentation** tab of the plan.

4.  Select **Create new section**.

    You can add a documentation section in the business continuity plan.

    If you create a documentation section and move away without saving the changes, the documentation section is marked as **Untitled** with the **Unsaved changes** tag as shown in the example. A message is displayed on the screen: `Do you want to save the changes?`

    ![Save the documentation section.](../image/bcp-doc-section-save-changes.png)

    If you select **Save**, the documentation section is saved in the plan. If you select **Discard**, the changes to the documentation section are not saved.

5.  To create a documentation section, select **Create**.

    The example shows the Overview and BCP Checklist documentation sections in a business continuity plan. The Overview documentation section has an order value of 0. The BCP Checklist documentation section has an order value of 100.

    **Note:** When you create a documentation section on the **Documentation** tab without using the plan template, the **Reset to template** UI action is not available for that documentation section.

    ![Order field in the documentation section of a BCP.](../image/bcp-doc-section-order-field.png)

    To create a documentation section that is displayed as the second section in the Sections panel, assign it an order value that is more than 0 and less than 100, such as 50.

    The documentation section with an order value of 50 is displayed as the second documentation section in the Sections panel on the **Documentation** tab.

    ![Middle order of the doc section.](../image/bcp-doc-section-middle-order.png)

6.  To save the documentation section in the plan, select **Save section**.

    The documentation section is saved in the business continuity plan.

    ![Saving the documentation section.](../image/bcp-new-doc-section-saved.png)

7.  To delete a documentation section in the plan, select **Delete**.

8.  To reset a documentation section to its template, select the More actions \(**...**\) icon and then select **Reset to template**.


**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

