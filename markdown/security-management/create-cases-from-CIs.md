---
title: Create a case from CIs
description: You can create a security case from configuration items in the Configuration Item \[cmdb\_ci\] table. After the CIs have been used to create a new case, you can use Security Case Management to analyze the data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuration items in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Create a case from CIs

You can create a security case from configuration items in the Configuration Item \[cmdb\_ci\] table. After the CIs have been used to create a new case, you can use Security Case Management to analyze the data.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## About this task

You need to navigate to the configuration items you want to use to create a case.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Base Items** &gt; **Computers** to view CIs for computers.

    The list for the selected CI type opens. From the list, you can create a new case from one or more CIs, or you can select a specific CI and create a new case from the form.

2.  From the list, select the CIs you want added to a new case.

3.  From the **Actions on selected items** drop-down list, select **Add to Security Case**.

    ![Add a CI to a new case](../image/add-ci-to-new-case.png)

    The **Add to Security Case** dialog box opens. If you already have cases assigned to you, they display in the list.

    ![Add a CI to a new case](../image/add-ci-to-case.png)

4.  Click **Create New Case**.

5.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Case Name|Enter a name for this case.|
    |Description|Enter a description that would be of value to the case analyst.|

6.  Click **Submit**.

    A message at the top of the list indicates that a new case has been created, along with a link to the case in Security Case Management.

7.  Click the link to view the new case.


**Parent Topic:**[Configuration items in cases](../concept/cases-from-cis.md)

**Related topics**  


[Add CIs to existing cases](add-cis-to-cases-sir.md)

