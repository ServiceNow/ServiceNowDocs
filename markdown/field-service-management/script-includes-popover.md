---
title: Customize the popover fields on the calendar in Dispatcher Workspace
description: Add or remove the fields that show in Dispatcher Workspace popovers so more relevant information is easier for dispatchers to find.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize Dispatcher Workspace with UI Builder, Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Customize the popover fields on the calendar in Dispatcher Workspace

Add or remove the fields that show in Dispatcher Workspace popovers so more relevant information is easier for dispatchers to find.

## Before you begin

Role required: wm\_admin

## About this task

**Warning:** Only developers with a high level of experience using JavaScript should perform this procedure.

Using JavaScript along with a script includes, you can show different values than the default information that is shown in the popover window. The default fields in the popover information are:

-   **Short description**: A short description of the work order task
-   **Number**: The work order task number
-   **Scheduled start**
-   The **Assignment group**
-   **Location**: The location of the work order task

The following image shows that the **Assigned to** field has been added to the pop over window to indicate who the work order task is assigned to.

![Modified pop over with the Assigned to field added](../image/modified_popover.png)

## Procedure

1.  Find the values of the fields you want to add.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  In the **Search** field, search for the table with the relevant type of information.

        -   Work order task values: wm\_task
        -   Schedule values: cmn\_schedule\_span
        -   Personal event values: sn\_shift\_planning\_agent\_schedule\_request
    3.  Open the relevant table and copy the value that you want to display.

2.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

3.  In the **Search** field, enter `DispatcherWorkspaceCalendarBrokerImplSNC` and open the record.

4.  Scroll to the `getCalendarEventTooltipDetails` function.

5.  Select and copy the entire `getCalendarEventTooltipDetails` function.

6.  Return to **All** &gt; **System Definition** &gt; **Script Includes**.

7.  In the **Search** field, enter `DispatcherWorkspaceCalendarBrokerImpl` and open the record.

8.  Paste the `getCalendarEventTooltipDetails` function into the `DispatcherWorkspaceCalendarBrokerImpl` record beneath where it says `//Add / override customizations here.`.

9.  Add or remove the fields you want.

10. Select and hold \(or right-click\) in the header of the page and select **Save**.


