---
title: Fetch Workday reports
description: As an administrator, fetch the reports metadata from other business applications such as Workday. View the Workday reports, leaves, compensation, and other information from your ServiceNow instance.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Approvals hub integration with Workday, Approval hub integrations, Integrate, Employee Center, Employee Service Management]
---

# Fetch Workday reports

As an administrator, fetch the reports metadata from other business applications such as Workday. View the Workday reports, leaves, compensation, and other information from your ServiceNow instance.

## Before you begin

Role required: sn\_hr\_workday.admin, sp\_admin, and sn\_hr\_integr\_fw.admin

## Procedure

1.  Navigate to **All** &gt; **Workday Pull To-dos** &gt; **Configuration Workday Approval Todos** and set the **Active** value to **True** to run the reports.

2.  Configure the **Load interval** and **Initial load start date time** as explained in [Configure Workday to-dos](config-workday-raas-report.md).

3.  Activate the schedule flow that pulls data from Workday as explained in [Activating schedule flows](../../human-resources/task/activate-w-schedule-flow.md).

    Based on the configuration and permissions, the data with new records and any changes to the existing records is pulled into the staging records.

4.  Verify the progress of the job from **All** &gt; **Workday Pull To-Dos** &gt; **Workday Integration Job Tracker.**

    For more information, see [View job tracker details from Workday](../../human-resources/task/w-job-tracker.md) and [View tasks from Workday](../../human-resources/task/view-to-dos-wd.md).

5.  Navigate to **All** &gt; **System Definition** &gt; **Tables** to check the staging, todos, and todos items records.

    Here is an example for Compensation change request. You can see the similar records for other to-do configurations.

    -   Compensation Change Request Staging \[**sn\_hr\_workday\_compensation\_change\_request\_staging**\]
    -   Compensation Change Request ToDos \[**sn\_hr\_workday\_compensation\_change\_request\_todos**\]
    -   Compensation Change Request ToDos Items \[**sn\_hr\_workday\_compensation\_change\_request\_todos\_items**\]
6.  See the sample Workday report and its metadata.

    After data is pulled into staging tables, use transform maps to move data into target tables.

    **Note:** If event data does not appear on the Workday event table, check the Workday credentials. If credentials are fine, check **Run Workday Integration Flow** flow execution and **Workday Pull-Todos Scheduled Import** subflow execution for more information.

7.  Use transform maps and verify data relationships between source table and target table as explained in [Use transform maps](../../human-resources/reference/transform-maps-w.md).

    The fetched data is now transformed for display on **My tasks**.

    **Note:** When the todos do not load on my tasks page, verify the data transformation in the staging, todos, and todos items records. If you see issues, see credentials and flow execution for more information.


## Result

The Workday integration syncs the requests automatically and transforms the data to display the pending Workday open requests on **My tasks**.

## What to do next

Proceed to **To-dos Configuration** and use the default **Approval \| Workday** task configuration.

For data protection, use the default purge policy to delete data more often. By default, data purge happens once in 30 days.

**Note:** To protect sensitive data, ensure you remove the HR administrator role from IT administrator. This step ensures that only the HR administrator \[sn\_hr\_core.admin\] has access to the sensitive information. Ensure only the HR administrator \[sn\_hr\_core.admin\] has access to the sensitive information as explained in [Remove HR Administrator role from IT System Administrators](../../human-resources/task/t_HRRemoveAdminRole.md)

-   Only the open requests are displayed on the approvers **My tasks** page.
-   Changes to the reports and requests reflect when the approver selects the open task.

**Parent Topic:**[Approvals hub integration with Workday](../concept/wd-ec-integration.md)

