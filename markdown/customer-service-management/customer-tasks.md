---
title: Customer tasks
description: From the Customer Service Portal, external users can view projects, complete assigned tasks, and create cases for project issues.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating with Customer Project Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Customer tasks

From the Customer Service Portal, external users can view projects, complete assigned tasks, and create cases for project issues.

A user must have one of the following CSM external roles to perform the tasks described in the following table:

-   sn\_customerservice.customer
-   sn\_customerservice.customer\_admin
-   sn\_customerservice.partner
-   sn\_customerservice.partner\_admin

<table id="table_ddt_n4l_hkb"><thead><tr><th>

Task

</th><th>

Details

</th></tr></thead><tbody><tr><td>

View projects and project details

</td><td>

Customers can view the projects created for their accounts if they have been associated with the project as a project contact. Customers have read-only access to project details on the Customer Project form. Customers can also view records in the following related lists if the system administrator has configured the corresponding ACLs for each of the tables.

-   Customer Project Tasks
-   Project Change Requests
-   Status Reports
-   Sub Projects
-   Work Orders
-   Project Contacts

 **Note:** The Work Orders related list is displayed if the following plugins are active: Field Service with Project Management \(com.snc.wm\_ppm\) and Customer Service with Field Service Management \(com.snc.csm\_fsm\_integration\).

 To view projects:

1.  Click **Support** in the Customer Service Portal header.
2.  Click **Projects** and select a project from the Customer Projects list.
3.  View the details in the Customer Project form.

</td></tr><tr><td>

View and update project tasks

</td><td>

Customers can view project tasks for the projects that have been created for their accounts if:

-   They have been associated with the project as a project contact.
-   The project tasks have been marked as **Visible to customer**.

Customers can view and update project tasks that have been assigned to them by the customer project manager.

 To view and update project tasks:

1.  Click **My Lists** in the Customer Service Portal header.
2.  Click **My Project Tasks** and select a task from the Customer Project Tasks list.
3.  View the details in the Customer Project Task form.
4.  Update the **Actual start date** and **Actual end date** fields as needed and click **Save**.
5.  Add a comment in the **Activity** field and click **Post**.

**Note:** Customers can also view tasks directly from **Support** &gt; **Projects** &gt; **Project Tasks**.

</td></tr><tr><td>

Complete project tasks

</td><td>

When a customer completes the work for a project task, they can mark the task as complete. 1.  Click **My Lists** in the Customer Service Portal header.
2.  Click **My Project Tasks** and select a task from the Customer Project Tasks list.
3.  Click **Mark Complete** in the Actions widget.

</td></tr><tr><td>

Create cases for projects and project tasks

</td><td>

Customers can create cases for projects and project tasks if they have been associated with a project as a project contact. Customers can create cases in two ways: -   From a project or project task form.
-   From the Case menu in the Customer Service Portal header.

 To create a case from a project or project task:

1.  Navigate to a Customer Project form or a Customer Project Task form.
2.  Click **Create Case** in the Actions widget.
3.  Fill in the fields on the Create Project Case record producer. The **Project** and **Project Task** fields are auto populated.
4.  Click **Submit**.

 To create a case from the Case menu.

1.  Click **Case** in the Customer Service Portal header and select **Create Project Case**.
2.  Fill in the fields on the Create Project Case record producer.
3.  Click **Submit**.

 The Create Project Case record producer includes **Project** and **Project Task** fields. These fields are displayed if a customer has access to any of the project tasks. Project and project task selection is limited to the projects for the customer's account.

</td></tr><tr><td>

View a list of cases created for the projects and project tasks for an account

</td><td>

Customer administrators, partner administrators, and customer case managers can see all of the cases that have been created for the projects and project tasks for an account. 1.  Click **My Lists** in the Customer Service Portal header.
2.  Click **All Cases** in the My Lists widget.

</td></tr><tr><td>

View the project change request and project issue records created for a case

</td><td>

Customer contacts can view the project change request and project issue records that have been created for a case if:-   They have been added to a project as a project contact.
-   The system administrator has configured the corresponding ACLs for each of the tables.

 1.  Click **My Lists** in the Customer Service Portal header.
2.  Click **All Cases** in the My Lists widget.
3.  Select a case from the Cases list.
4.  View the records in the Related Records widget.

</td></tr></tbody>
</table>