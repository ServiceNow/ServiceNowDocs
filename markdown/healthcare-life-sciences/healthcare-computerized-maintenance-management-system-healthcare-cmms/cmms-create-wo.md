---
title: Create a work order for a medical device issue case
description: Create a work order to specify the nature of the work required to resolve a medical device issue case.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing medical device issue cases in Workspace, Managing medical device cases in Workspace, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Create a work order for a medical device issue case

Create a work order to specify the nature of the work required to resolve a medical device issue case.

## Before you begin

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](../concept/clinical-device-mgmt-overview.md).

Role required: sn\_hcls\_cmms.clinical\_engineer

## Procedure

1.  Open your Workspace by navigating to **All** &gt; **Healthcare CMMS** &gt; **Workspace**.

2.  Go to **Lists** &gt; **Medical device issue case** &gt; **All**.

3.  Click the link to the case for which you want to a create work order.

4.  On the Details tab, click **Create Work Order**.

5.  On the Work Order tab, describe the work requested in the **Short description** and **Description** fields.

6.  Fill in the other details such as location where work is required, template for creating the work order, and skills required to complete the work order.

7.  In the **Requested due by** field of the Scheduling section, click the ![Show calendar icon.](../image/show-calendar-icon.png) and select enter a date and time by when the work order must be completed.

8.  Click **Ready For Qualification**.


## Result

A work order task is automatically created. The short description, description, and location of the work order are copied into the task.

## What to do next

A user with the sn\_hcls\_cmms.clinical\_engineering\_technician role can then complete the work order task. For more information, see [Managing work orders and work order tasks](https://www.servicenow.com/docs/access?context=managing-work-orders&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

After the work order task is completed, you can close the case. For more information, see [Close a medical device issue case](cmms-close-cd-issue-case.md).

