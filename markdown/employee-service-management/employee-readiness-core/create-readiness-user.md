---
title: Create health and safety user records
description: Create health and safety user records to track requirement statuses for all employees and visitors.
locale: en-US
release: zurich
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Employee Health and Safety Status, Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create health and safety user records

Create health and safety user records to track requirement statuses for all employees and visitors.

## Before you begin

If the ServiceNow® Customer Service Management \(CSM\) application is activated, you can also create health and safety user records for consumers and contacts.

Role required: sn\_imt\_core.admin

## About this task

Health and safety user records are automatically created for users \[sys\_user\] with activity or an assigned role in any of the following Safe Workplace suite and Emergency Response Management applications.

-   Contact Tracing
-   Emergency Outreach
-   Employee Health Screening
-   Employee Readiness Core
-   Employee Travel Safety
-   Health and Safety Testing
-   Safe Workplace Dashboard
-   Vaccination Status
-   Workplace PPE Inventory Management
-   Workplace Core

Health and safety user records are also created for visitors who are invited through the Employee Readiness Core app.

Some users might not have activity or assigned roles in the apps, so health and safety user records are not automatically created for them. If you want to view the requirement status for these users, you can manually create health and safety user records for them.

## Procedure

1.  Navigate to **All** &gt; **Employee Health and Safety Status** &gt; **Health and Safety Users**.

2.  Click **New**.

3.  In the **type** field, select **Visitor** or **Employee**.

    **Note:** If you're creating a health and safety user record for a CSM consumer or contact, select **Employee**.

4.  Select a value in the **User** or **Visitor** field.

    -   If you're creating a record for an employee,consumer, or contact, select the user in the **User** field.
    -   If you're creating a record for a visitor, select the visitor in the **Visitor** field.
5.  Select a value in the **Working location type** field.

    -   If the user is reporting to your organization on-site full time, select **Full time on-site**.
    -   If the user is reporting to your organization remotely full time, select **Full time remote**.
    -   If the user is reporting to your organization part time remote and part time on-site, select **Part time remote**.
6.  Click **Submit**.

    The **Requirement status** field is read-only and is updated after you submit the record.

    The user or visitor is added to the Health and Safety User table \[sn\_imt\_core\_health\_and\_safety\_user\]. A record is created for the user or visitor in the Employee Health and Safety Requirement table \[sn\_imt\_core\_employee\_health\_and\_safety\_requirement\] for each active requirement using the default status for the requirement.


## What to do next

You can view all health and safety user records by navigating to **Employee Health and Safety Status** &gt; **Health and Safety Users**. The **Requirements status** column shows the user's or visitor's progress towards completing all active requirements. The value is **Cleared** if they have fulfilled all active requirements. The value is **Not cleared** if they are missing any requirements.

You can also look up the requirements status for individual users or visitors by navigating to **Employee Health and Safety Status** &gt; **View Employee and Visitor Status**. The status page can be used during the health screening process for entry to a location. For more information, see [Conduct a health screen for entry](../../employee-health-screening/task/screen-returning-employee.md).

**Parent Topic:**[Employee Health and Safety Status](../concept/employee-health-safety-status.md)

