---
title: Add security incidents to an existing case
description: You can add security incidents to one or more existing cases. After the security incidents have been added to cases, you can use Security Case Management to analyze the data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security incidents in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Add security incidents to an existing case

You can add security incidents to one or more existing cases. After the security incidents have been added to cases, you can use Security Case Management to analyze the data.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## About this task

You need to navigate to the security incidents you want to add to existing cases.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show Open Incidents**.

    The Security Incidents list opens.

2.  In the list, select one or more security incidents that you want to add to existing cases.

    **Note:** If you select multiple security incidents, the selected security incidents are added to each of the selected cases.

3.  From the **Actions on selected items** drop-down list, select **Add to Security Case**.

    The **Add to Security Case** dialog box opens and displays the cases assigned to you.

    ![Add a security incident to an existing case](../image/add-sec-inc-to-existing-case.png)

4.  Select the cases into which you want to add the selected security incidents.

5.  Click **Add**.

    A message indicates that the selected records have been added to the cases, along with a link to the cases in Security Case Management.


**Parent Topic:**[Security incidents in cases](../concept/case-in-sir.md)

**Related topics**  


[Create a case from security incidents](create-cases-from-security-incidents.md)

