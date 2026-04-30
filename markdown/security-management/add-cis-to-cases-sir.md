---
title: Add CIs to existing cases
description: You can add configuration items to one or more existing cases. After the CIs have been added to cases, you can use Security Case Management to analyze the data.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuration items in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Add CIs to existing cases

You can add configuration items to one or more existing cases. After the CIs have been added to cases, you can use Security Case Management to analyze the data.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## About this task

You need to navigate to the CIs you want to add to the existing cases.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Base Items** &gt; **Computers** to view CIs for computers.

    The list of the selected CIs opens.

2.  In the list, select one or more CIs that you want to add to existing cases.

    **Note:** If you select multiple CIs, the selected CIs are added to each of the selected cases.

3.  From the **Actions on selected items** drop-down list, select **Add to Security Case**.

    The **Add to Security Case** dialog box opens and displays the cases assigned to you.

    ![Add a CI to a case](../image/add-ci-to-case.png)

4.  Select the cases into which you want to add the selected CIs.

    ![Add CIs to an existing case](../image/add-ci-to-existing-cases.png)

5.  Click **Add**.

    A message indicates that the selected records have been added to the cases, along with a link to the cases in Security Case Management.


**Parent Topic:**[Configuration items in cases](../concept/cases-from-cis.md)

**Related topics**  


[Create a case from CIs](create-cases-from-CIs.md)

