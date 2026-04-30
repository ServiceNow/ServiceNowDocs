---
title: Create a case from affected users
description: You can create a security case from affected users in the User \[sys\_user\] table. After the affected users have been used to create a new case, you can use Security Case Management to analyze the data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Affected users in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Create a case from affected users

You can create a security case from affected users in the User \[sys\_user\] table. After the affected users have been used to create a new case, you can use Security Case Management to analyze the data.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## About this task

You need to navigate to the users you want to use to create a case.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

    The list for the selected users opens. From the list, you can create a new case from one or more user records, or you can select a specific user record and create a new case from the form.

2.  From the list, select the users you want added to a new case.

3.  From the **Actions on selected items** drop-down list, select **Add to Security Case**.

    ![Add a user to a new case](../image/add-user-to-new-case.png)

    The **Add to Security Case** dialog box opens. If you already have cases assigned to you, they display in the list.

    ![Add a user to a new case](../image/add-user-to-case.png)

4.  Click **Create New Case**.

5.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Case Name|Enter a name for this case.|
    |Description|Enter a description that would be of value to the case analyst.|

6.  Click **Submit**.

    A message at the top of the list indicates that a new case has been created, along with a link to the case in Security Case Management.

7.  Click the link to view the new case.


**Parent Topic:**[Affected users in cases](../concept/cases-from-affected-users.md)

**Related topics**  


[Add affected users to existing cases](add-users-to-cases-sir.md)

