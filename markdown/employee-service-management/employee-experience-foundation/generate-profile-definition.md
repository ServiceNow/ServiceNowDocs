---
title: Create an active employee definition
description: Create an active employee definition to generate the employee profiles.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Employee profile, Setup task management, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Create an active employee definition

Create an active employee definition to generate the employee profiles.

## Before you begin

After you install the employee profile, create an active employee definition to opt in the new unified employee profile. An active employee definition is a condition that determines who an employee is. You can have only one active employee definition per domain.

**Note:** The employee definition table is domain-separated.

Role required: sn\_employee.admin

## Procedure

1.  Navigate to **Employee Profile** &gt; **Employee Definition**.

2.  On the employee definition page, click **New**.

3.  Select one of the available **Table** options.

    -   To create an employee definition from a user table, select **User**.
    -   To create an employee definition from HR records, select **HR Profile**.

        **Note:** The HR profile table is available only when you install the Human Resources Scoped App: Core \[com.sn\_hr\_core\] plugin.

4.  Create a condition from the available filters and clauses.

    For example, make sure that the **First name** starts with **All** to generate the employee profiles that match that condition.

    **Note:** The employee definition condition should be on the indexed columns. Also, keep the condition simple by using only a few filters.

5.  To mark the employee definition as active, select **Active**.

6.  Click **Save**.

    The **Generate Employee Profiles** option appears with the following message stating that you can regenerate the employee profiles as per the updated definition and generate employee profiles.

    **Note:** When you have multiple employee definitions, ensure you deactivate the current active definition before activating the other.

7.  Click **Generate Employee Profiles**.

    The confirmation appears stating that employee profiles are being created.

    After you install the employee profile, create an active employee definition to opt in the new unified employee profile. An active employee definition is a condition that determines who an employee is. You can have only one active employee definition per domain.


## Result

Once employee profiles are generated, you receive an email with the count and the link to view the employee profiles. Verify the new employee profiles created based on your active employee definition from the **Employee Profiles** table. You can also sync profile generation periodically.

**Note:** Employee profiles are added incrementally when the active employee definition matches; for any new users that are added to the user table after generating the employee profiles.

## What to do next

Once you have employee definition, you can proceed to opt for the employee profile.

