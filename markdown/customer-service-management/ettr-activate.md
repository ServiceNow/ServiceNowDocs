---
title: Display the time to resolve ribbon component
description: Activate the ETTR Experience Card so that you can display the time to resolve ribbon component in your CSM workspaces.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure settings for estimated time to resolve values, Estimated time to resolve a case, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Display the time to resolve ribbon component

Activate the **ETTR Experience Card** so that you can display the time to resolve ribbon component in your CSM workspaces.

## Before you begin

Role required: admin

## About this task

The Time to resolve ribbon component is available by default and can be displayed in both CSM Agent Workspace and CSM Configurable Workspace. You must activate the component in CSM Agent Workspace before you activate it in CSM Configurable Workspace.

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Forms** &gt; **Workspace Ribbon Settings**.

2.  Select any record that has the table value **Case \[sn\_customerservice\_case\]**.

3.  Increase or decrease the values in the width column to make the total combined width of all the components to 12 or less.

    **Note:** If the total is already exceeding 12, decrease the values for the other components before modifying the value of **ETTR Experience Card**.

4.  Select **ETTR Experience Card**.

5.  Select **Active**.

6.  In the **Ribbon Component Attributes** form section, modify components such as the **Card title** and **Info message** as required.

    **Note:**

    -   You can see that the Solution name is pre-filled with the default name.
    -   The same procedure applies to activate the **ETTR Experience Card** in the CSM Configurable Workspace. You must activate the **ETTR Experience Card** in the CSM Agent Workspace before activating it in the CSM Configurable Workspace. Navigate to **User Experience Framework** &gt; **Ribbon Configuration Settings** and activate. The **Ribbon Component Attributes** section is not available for modifying.

