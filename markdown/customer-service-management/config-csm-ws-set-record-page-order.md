---
title: Set record page order
description: Set the order number of a record page and activate the record page to determine the default page for displaying records in CSM Configurable Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Set record page order

Set the order number of a record page and activate the record page to determine the default page for displaying records in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

Each record page has an order number and can also be set to active or inactive. The active record page with the lowest order number is the default page. When the system displays a record in CSM Configurable Workspace, it uses this default page to display the record information.

|Record page|Order|
|-----------|-----|
|Record default|0|
|Interaction record Page|100|
|CSM default record page|-1000|
|CSM Interaction record page|-1000|
|Front-line case page|1000|

To use a different page as the default page, you need to manually switch from the existing pages to the new pages by changing the page order number.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **CSM/FSM Configurable Workspace** experience.

3.  Select the desired page in the Variants list, for example, **CSM default record page**.

4.  Set the page order.

    1.  Select the additional actions menu for the page and then select **Edit conditions**.

    2.  Enter a value in the **Order** field.

    3.  Select **Save**.

5.  Activate the page.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

    2.  Select the **CSM/FSM Configurable Workspace** experience.

    3.  In the **Admin panel** field, open the UX App Configuration: CSM/FSM Configurable Workspace App Config record.

    4.  Locate the page in the UX Screens related list.

    5.  Set the **Active** field to true.


