---
title: Adding the Discuss button for non-task tables
description: To use Sidebar in non-task tables, follow this procedure to add the Discuss button to the layout.
locale: en-US
release: yokohama
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Adding the Discuss button for non-task tables

To use Sidebar in non-task tables, follow this procedure to add the Discuss button to the layout.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_declarative_action_assignment.list` in the filter navigator.

2.  Filter the Action Label values that contain Open create collab chat modal.

3.  Select the record result that you want to edit.

4.  From the Open create collab chat modal Action Assignment, scroll down to Related Links and select the UX Add-on Event Mappings tab.

5.  Open the UX Add-on Event Mapping record and verify if the Application field uses the Common Page Template.

6.  Create a new UX Add-on Event Mapping by copying all field values from the base level Open create collab chat record including Source element ID, Source declarative Action, Target Event and Target Payload Mapping.

7.  Search for the custom Parent Macroponent that your organization uses if needed.

8.  Select **Save**.

9.  If you’re unsure of UX Macroponent being used within your Configurable Workspace, you can look up the Definition Record by navigating to UI Builder, selecting Menu &gt; Developer &gt; Open page definition.


