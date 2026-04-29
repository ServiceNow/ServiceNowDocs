---
title: Set record page order
description: Set the order value of a record page to determine the default page for displaying records in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Record pages, Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Set record page order

Set the order value of a record page to determine the default page for displaying records in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

Record pages can be active or inactive. Each record page also has an order value. The active record page with the lowest order number is the default page. When the system displays a record in CSM Configurable Workspace, it uses this default page to display the record information.

|Record page|Order|
|-----------|-----|
|CSM default record page|-1000|
|CSM Interaction record page|-1000|
|Email interaction record page|-1001|
|Front-line case page|1000|
|CSM voice interaction record page|2000|
|CSM centered chat interaction record page|-2001|
|Record default|0|
|Interaction record Page|100|

To use a different page as the default page, you need to manually switch from the existing page to the new page by changing the page order value.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **CSM/FSM Configurable Workspace** experience.

3.  Select the desired page in the Variants list, for example, **CSM default record page**.

4.  Set the page order value.

    1.  Select the additional actions menu for the page and then select **Edit conditions**.

    2.  Enter a value in the **Order** field.

    3.  Select **Save**.

5.  Activate the page.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

    2.  Select the **CSM/FSM Configurable Workspace** experience.

    3.  In the **Admin panel** field, open the UX App Configuration: CSM/FSM Configurable Workspace App Config record.

    4.  Locate the page in the UX Screens related list.

    5.  Set the **Active** field to true.


**Related topics**  


[CSM Configurable Workspace record pages](../concept/csm-config-workspace-record-pages.md)

