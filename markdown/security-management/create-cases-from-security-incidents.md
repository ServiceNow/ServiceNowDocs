---
title: Create a case from security incidents
description: In Security Incident Response, you can create cases from security incidents. After the security incidents have been used to create a new case, you can use Security Case Management to analyze the data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security incidents in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Create a case from security incidents

In Security Incident Response, you can create cases from security incidents. After the security incidents have been used to create a new case, you can use Security Case Management to analyze the data.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## About this task

You need to navigate to the security incidents you want to use to create cases.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show Open Incidents**.

    The Security Incidents list opens. From the list, you can create a new case from one or more security incidents, or you can select a specific security incident and create a new case from the form.

2.  To create a case from the list, select the artifacts you want added to a new case.

3.  From the **Actions on selected items** drop-down list, select **Add to Security Case**.

    ![Add security incidents to a new case](../image/add-sec-inc-to-case.png)

    The **Add to Security Case** dialog box opens. If you already have cases assigned to you, they display in the list.

    ![Add security incident to case](../image/add-sec-inc-case-dialog.png)

4.  Click **Create New Case**.

5.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Case Name|Enter a name for this case.|
    |Description|Enter a description that would be of value to the case analyst.|

6.  Click **Submit**.

    A message at the top of the list indicates that a new case has been created, along with a link to the case in Security Case Management.

7.  Click the link to view the new case.


**Parent Topic:**[Security incidents in cases](../concept/case-in-sir.md)

**Related topics**  


[Add security incidents to an existing case](add-sec-inc-to-cases.md)

