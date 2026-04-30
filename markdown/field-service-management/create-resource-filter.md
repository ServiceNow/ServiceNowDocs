---
title: Create an advanced resource filter for dispatchers
description: Create an advanced resource filter so all dispatchers can use the same filter in Dispatcher Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring advanced resource filters for Dispatcher Workspace, Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Create an advanced resource filter for dispatchers

Create an advanced resource filter so all dispatchers can use the same filter in Dispatcher Workspace.

## Before you begin

Role required: admin

## About this task

When administrators create an advanced resource filter for dispatchers they show up in the Resource filter drop-down menu in Dispatcher Workspace. All advanced filters created by administrators show up alphabetically at the top of the resource filters list. Dispatcher created filters show below the list of administrator filters.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace Configuration** &gt; **Resource Filter**.

2.  Select **New**.

3.  Fill in the fields in the form:

    -   Title: The name of the filter that will show in Dispatcher Workspace.
    -   Active: if the filter is active.
4.  Select **Submit**.

5.  Select the name of the filter you just created.

6.  Select **New**.

7.  Fill in the fields on the form:

    -   Table: Select either the agent\_filter\_config\_view or the crew\_filter\_config\_view.
    -   Filter: Add the conditions and clauses that will be used to filter the information in the table you selected.

8.  Select **Submit**.

    The filter is added to dispatcher workspace for dispatchers to use.


