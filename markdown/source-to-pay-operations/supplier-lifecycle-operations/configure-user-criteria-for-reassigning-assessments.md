---
title: Configure user criteria for reassigning assessments
description: You can configure the user criteria for reassigning assessments to restrict reassignment within the organization.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-02-22"
reading_time_minutes: 1
breadcrumb: [Configure smart assessments, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure user criteria for reassigning assessments

You can configure the user criteria for reassigning assessments to restrict reassignment within the organization.

## Before you begin

The reassignment user criteria are configured based on the **Audience type** of the assessments.

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment workspace**.

2.  Open the assessment template for which you have to configure the user criteria for reassigning assessments.

3.  Open the **related lists** for the assessment template by right clicking the assessment name and selecting **Configure** &gt; **Related Lists**.

    ![Opening related lists for the assessment template](../image/related-links.png)

4.  Add **User criteria** to the selected related list and **Save** the form.

    ![Add User criteria field to the assessment template](../image/slo-user-criteria.png)

5.  In the **User criteria** section of the assessment template, select **Edit** to update the user criteria list.

    ![Edit button in User criteria section](../image/slo-user-criteria-list.png)

6.  Add the required roles or configurations to the User criteria based on the Audience type and save the template.

    |Audience type|User criteria|
    |-------------|-------------|
    |**Only primary supplier contact\(s\)**|**Supplier: Primary Contact** \(predefined\)|
    |**All supplier contacts**|**Supplier: Any Contact** \(predefined\)|
    |**Manager\(s\)**|Set the custom criteria for primary supplier managers. For more information, see [Create custom user criteria for primary managers](../task/create-new-user-criteria.md).|
    |**All supplier managers**|Set the custom criteria for all supplier managers. For more information, see [Create custom user criteria for all managers](../task/create-user-criteria-all-managers.md).|

    For example: For the audience type **All supplier contacts**, add **Supplier: Any Contact** to the user criteria list and save the template.

    ![Add Supplier: Any Contact to the user criteria list.](../image/slo-user-criteria-supplier.png)

7.  Set the status of the user criteria to active.

8.  Publish the assessment template.


## What to do next

Create segmentation rule, map it to the assessment template, and create assessments from the Source-to-Pay workspace.

-   **[Create custom user criteria for primary managers](../task/create-new-user-criteria.md)**  
You can create custom user criteria for primary relationship managers for configuring the assessment reassignment criteria.
-   **[Create custom user criteria for all managers](../task/create-user-criteria-all-managers.md)**  
You can create custom user criteria for all managers for configuring the assessment reassignment criteria.

**Parent Topic:**[Configure smart assessments](configure-smart-assessments.md)

