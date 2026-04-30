---
title: Configure tabs in the contextual side panel
description: Use the inlineTabExclusion UX page property to prevent tabs from appearing in the configurable side panel in CSM Configurable Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure tabs in the contextual side panel

Use the **inlineTabExclusion** UX page property to prevent tabs from appearing in the configurable side panel in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

You can configure the **inlineTabExclusion** UX page property for specific tables. The following example shows the default value for this property.

```
[{
  "template": [
    "incident","sn_customerservice_case"
  ],
  "attachment": [
    "sn_customerservice_case"
  ]
}]
```

In the mapping for this property, the key represents the tab to be hidden and the value includes the list of tables for which the tab is hidden. In the above example:

-   The Response template tab is hidden for the Incident \[incident\] and Case \[sn\_customerservice\_case\] tables.
-   The Attachment tab is hidden for the Case \[sn\_customerservice\_case\] table.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  Select the **CSM/FSM Configurable Workspace** experience.

3.  In the UX Page Properties related list, select **inlineTabExclusion**.

4.  Make the necessary changes to the **Value** field.

5.  Select **Update**.


