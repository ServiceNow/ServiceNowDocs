---
title: Create a comprehensive lifecycle report using a guided experience
description: Use a guided experience to improve your lifecycle data completeness.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create a comprehensive lifecycle report using a guided experience

Use a guided experience to improve your lifecycle data completeness.

## Before you begin

Role required: sam\_admin or sam\_user

## About this task

This playbook is divided into four stages:

-   Getting ready
-   Engage content service
-   Use built-in tools
-   Finalize report

Each stage has one or more than one activity that you need to perform. Activities are typically performed sequentially. You can go back to those activities to complete them later.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics**.

2.  Select the **Lifecycle management** tab.

3.  Select **Add lifecycle data** to open the Add data with playbookdialog box.

4.  Select one or more publishers and products in the **Publishers** and **Products** fields.

    You can also select the **All publishers** and **All products** check boxes to include all the publishers and products.

5.  Select a product type for the lifecycle data in the **Product type** section.

6.  Select a user to manage this playbook in the **Assigned to** field.

    The playbook can be assigned to only users with the sam\_admin or the sam\_user role.

7.  Enter a name for the playbook in the **Display name** field.

8.  Select **Start playbook**.

    The playbook opens in the Getting ready stage. Its current state is **In Progress**.

    The playbook displays the publishers and products that you selected. Additionally. the target completeness is also mentioned, which by default is 95%.

9.  Select **Mark Complete** to go to the next page.

    The Create a success goal page opens. Associating a success goal to your playbook helps you to track your work and contribute towards a complete lifecycle report.

10. On the form, fill in the fields.

    For a description of each field, see [SAM Success Goal Details](../reference/sam-success-goal-details.md).

11. Select **Save** to move to the next page.

    The Review report page opens listing all the lifecycle records for the particular publisher and product that you selected.

12. Select **Mark Complete** to go to the next page.

    All the tasks in the Getting ready lane are complete and you move to the Introduction page in the Engage content service stage.

13. Select **Mark Complete** to go to the next page.

    The Create success activity page opens. Create a success activity to associate it with the success goal you earlier created.

14. On the form, fill in the fields.

    For a description of each field, see [SAM Success Activity](../reference/sam-success-activity.md).

    If your role or any other role that has permission to submit content requests, can create and submit a content request.

    1.  Select the support portal link to open the Asset Management Content Request page in a new tab.
    2.  On the form, fill in the fields.
    3.  Select **Submit** to submit the content request and return to the Create success activity page.
15. Select **Submit** in the Create success activity page.

    The Follow up on task page opens.

16. Select **Mark Complete** to go to the next page.

    All the tasks in the Engage content service stage are complete and you move to the Introduction page in the Use built-in tools stage.

17. Select **Mark Complete** to go to the next page.

    The Input custom lifecycle dates page opens that lists lifecycle reports that don't have end-of-life, end of support, or end of extended support dates.

18. Select dates in the **Phase start dates** column.

    The dates you enter are automatically pushed into the Custom Software Product Lifecycle \[sam\_custom\_sw\_product\_lifecycle\] table.

19. Select **Mark Complete** to go to the next page.

    The Input custom GA dates page opens that lists lifecycle reports that don't have GA dates.

20. Select dates in the **Phase start dates** column.

    The dates you enter are automatically pushed into the Custom Software Product Lifecycle \[sam\_custom\_sw\_product\_lifecycle\] table.

21. Select **Mark Complete** to go to the next page.

    The Create lifecycle averages success activities page opens.

    The sam\_user role doesn't have permissions to create lifecycle averages. Create success activities instead and assign them to sam\_admin or other authorized users to create the lifecycle averages records.

    Users with the sam\_admin role have two options. They can create a success activity task and assign it to themselves for immediate completion, or they can assign the task to subject matter experts, such as Product Owners, who can provide guidance on the appropriate values and parameters. While sam\_admins have the technical permissions to create lifecycle average records, they may not have the domain expertise to determine the correct values for specific products.

22. Select **New** in the Create lifecycle averages success activities page.

23. On the form, fill in the fields.

    For a description of each field, see [SAM Success Activity](../reference/sam-success-activity.md)

24. Select **Submit** and then select **Mark Complete** to move to the Input lifecycle averages page.

    If you select **Mark Complete** before selecting **Submit**, you will be taken to the next page without submission of this task.

    You can review the existing lifecycle averages and update the values if needed or you can create a lifecycle averages record.

25. Select **New** to create a lifecycle averages record.

26. On the form, fill in the fields.

    For details, see [Create averages for product life cycles in workspace](create-lifecycle-averages-workspace.md).

27. Select **Submit** and then select **Mark Complete**.

28. Select **New** in the Create parent child definitions page.

    Create parent-child definitions to enable lifecycle date propagation across related software.

29. On the form, fill in the fields.

30. Select **Submit** then select **Mark Complete** to move to the Run report page.

    All the tasks in the Use built-in tools stage are complete and you move to the Run report page in the Finalize report stage.

31. Select **Mark Complete** to automatically initiate the **SAM - Create Calculated Software Lifecycles** job.

    After the job has successfully completed, the calculated lifecycles are created.

    If the job encounters errors, a troubleshooting message appears indicating that you need to execute the scheduled job manually from outside the playbook environment.

32. Select **Mark Complete** in the Calculated lifecycle job success page to automatically initiate the **SAM - Generate Data For Software Lifecycle Report** job.

    If the job encounters errors, a troubleshooting message appears indicating that you need to execute the scheduled job manually from outside the playbook environment.

33. Select **Mark Complete** once the job has successfully completed.

    The Review report page opens which shows the completeness score.

34. Select **Mark Complete**.

    This completes the playbook and you can exit the playbook.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

