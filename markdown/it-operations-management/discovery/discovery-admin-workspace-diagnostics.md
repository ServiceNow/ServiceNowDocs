---
title: Discovery Admin Workspace Diagnostics
description: Diagnostics allows you to prioritize and address Discovery schedule errors. Create and manage Error Tasks to track progress on resolving errors.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Diagnostics

Diagnostics allows you to prioritize and address Discovery schedule errors. Create and manage Error Tasks to track progress on resolving errors.

## Diagnostics

The **Diagnostics** page shows all errors from all discoveries. For each entry in the **Discovery errors** table, you can create a new Error Task or ignore the error with the **Create task** and **Ignore** buttons. Entries that already have an associated Error Task instead have an **Edit task** button and provide the task's name and priority.

Use the filter options to prioritize and address errors. You can filter by Discovery schedule with the **Schedule** drop-down menu, or search for the name of the error with the **Search** bar. The results can also be organized with the **Order By** drop-down menu in either ascending or descending order with the following options: Code, Priority, and Total Errors.

The error records can also be filtered with the **Filter** and **Has task** drop-down menus. In the **Filter** menu, you can choose to only show errors related to CMDB, Configuration, Credentials, Internal, or Network. Multiple categories can be selected at the same time. The **Has task** menu shows either all error records, those that have a task, or that do not have a task.

For each entry in the **Discovery errors** table, the **Total Errors** number can be selected to navigate to the **Error Stats Page**. The page provides information on the error and suggest **Instructions**, as well as an associated Knowledge Base article. If the error has an associated Error Task, its task number is displayed and can be accessed through its button.

The **Action** drop-down menu provides suggested actions based on the type of error, and is shared with the Error Task page. In the **Errors** table, the **Action on selected** drop-down menu can ignore individual IP addresses' errors, retry their discovery, add them to the global exclusion list, or check their Shazzam port status.

## Case management

The **Case management** page provides an overview of the statuses of Error Tasks. Each Error Task can be selected to navigate to their Error Task record. New tasks can be created and associated with existing errors using the **Create Task** button. The display style can be changed with **Kanban Board View** and **List View** buttons.

## Support tools

The **Support tools** page provides tools to investigate and troubleshoot your instance. The **CAPI to patterns** tool helps you migrate your Cloud Discovery from using Cloud API REST Calls to using Patterns. The **Probes to pattern migration** tool migrates older probes to use new, more flexible and efficient patterns. The **Detect frequently discovered CIs** tool deteremines which CIs are being discovered more often than others.

## Logs

The **Logs** page allows you to access the logs of the **ECC Queue**, **Discovery Logs**, and **Discovery Patterns Logs**. These logs can be filtered and each entry can be selected to view more details. Reviewing the logs can be useful in addressing diagnosing and addressing errors.

## Ignored errors

The **Ignored errors** page keeps a record of all errors ignored in the last 30 days. Errors older than 30 days are deleted. You can add an error back to the **Discovery errors** table using the **Undo ignore** button.

