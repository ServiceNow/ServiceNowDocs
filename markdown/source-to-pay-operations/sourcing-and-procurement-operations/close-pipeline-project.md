---
title: Close a pipeline project
description: As a sourcing manager, you can close the pipeline project when all the activities related to the sourcing pipeline project have been completed.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [close pipeline project]
breadcrumb: [Using Sourcing Pipeline Management, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Close a pipeline project

As a sourcing manager, you can close the pipeline project when all the activities related to the sourcing pipeline project have been completed.

## Before you begin

Ensure that you’ve qualified all the relevant suppliers, and have received all the bids and responses from them, before you begin the awarding process. At this point, the sourcing event that you plan to work on, and all its associated negotiations, sourcing requests, and purchase lines must be in the Requires Decision state.

Role required: sn\_shop.procurement\_specialist

## Procedure

1.  Navigate to **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and do one of the following:

    -   Navigate to **Lists** &gt; **My work** &gt; **Pipeline projects**.
    -   Navigate to **Lists** &gt; **All work** &gt; **Pipeline projects**.
3.  Open the pipeline project that is in the Work in progress state.

4.  Select **Close**.

    The system checks that all related objects, such as sourcing requests and sourcing events, are closed. If any of the related objects are open, an error message prompts you to close them.

    The Close pipeline project dialog box is displayed.

    ![Close pipeline project.](../image/pipeline-close.png)

    The **Hard savings** field is auto-populated and displays the cumulative savings from all sourcing events associated with the pipeline project. This value is calculated by summing the Negotiated savings from all closed purchase requisition lines \(PRLs\) within the sourcing events.

    If needed, you can edit the **Hard savings** field. If you edit the **Hard savings** field, a warning message appears indicating that the entered value differs from the cumulative negotiated savings on PRLs. This warning is shown only if there are negotiated savings on any PRL.

5.  Enter the project's financial data in the **Estimated spend**, **Hard savings**, **Targeted savings**, **Cost avoidance**, **Final spend**, **Other savings**, and **Lost savings** fields.

6.  In the **Closing notes** field, enter a brief summary of the pipeline project that provides context for future reference, auditing, or reporting.

7.  Select **Close**.

    The pipeline project moves to the Closed Complete state.


**Parent Topic:**[Using Sourcing Pipeline Management](../concept/use-pipeline-sourcing-mgmt.md)

