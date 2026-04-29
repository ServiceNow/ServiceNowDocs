---
title: Enable multi-store task plan templates
description: Complete the one-time administrator configurations required before multi-store task plan templates can generate cases across multiple retail locations.
locale: en-US
release: australia
product: \[Legacy\] Retail Task Management
classification: legacy-retail-task-management
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Configure, Retail Task Management, Retail]
---

# Enable multi-store task plan templates

Complete the one-time administrator configurations required before multi-store task plan templates can generate cases across multiple retail locations.

## Before you begin

Role required: admin

## About this task

Multi-store task plan templates create cases simultaneously across multiple service organizations. Three configurations must be in place before you can publish a multi-store template and generate cases: the **Affected Service Organizations** case field must be non-mandatory, the retail extension point implementation must be active, and the **Create multi entity records** UI action must be enabled.

## Procedure

1.  Make the Affected Service Organizations case field non-mandatory
2.  Navigate to **All** &gt; **sn\_case\_creation\_service\_org.list**.

3.  Select and hold \(or right-click\) the **Case** column header, then select **Configure** &gt; **Dictionary**.

4.  Open the dictionary entry for the **Case** field and clear the **Mandatory** check box.

5.  Select **Update**.

6.  Return to the **sn\_case\_creation\_service\_org** list, select and hold \(or right-click\) the column header, and select **Configure** &gt; **Form Layout**.

7.  Move the **Template Item** field from **Available** into **Selected**, then select **Save**.

8.  Verify the TaskTemplateServiceRetailImpl extension point implementation
9.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

10. Filter by **Application** = **Task Plan Templates** and open the **sn\_task\_plan.TaskTemplateService** extension point.

11. In the **Implementations** related list, confirm that **TaskTemplateServiceRetailImpl** is present and active.

    This implementation provides the `getEntitiesForTemplateItem` method, which queries the **Affected Service Organizations \[sn\_case\_creation\_service\_org\]** table by template item and returns the list of service organizations for which child cases are created.

12. Enable the Create multi entity records UI action
13. Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Form Actions**.

14. Search for `Multi` and open the **Create multi entity records** form action.

15. Confirm or set the **Server Script** field to the following value, then select **Update**.

    ```
    new sn_task_plan.MultiEntityCreationService().applyTaskTemplateForMultipleEntities(current, 'retail');
    ```

16. Confirm the action is active by verifying the **Active** check box is selected, then select **Update**.


## Result

The multi-store task plan template configuration is complete. Administrators can now publish a task plan template and select **Create multi entity records** to generate HQ Communications and In-Store Operations cases simultaneously across all affected service organizations.

