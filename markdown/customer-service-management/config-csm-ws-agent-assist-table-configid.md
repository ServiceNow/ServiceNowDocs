---
title: Configure the Agent Assist and Response Template tabs
description: Add a table configuration for the Agent Assist tab or Response Template tab for custom tables or custom case types in the contextual side panel in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-11"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure the Agent Assist and Response Template tabs

Add a table configuration for the Agent Assist tab or Response Template tab for custom tables or custom case types in the contextual side panel in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

The Agent Assist tab and the Response Template tab that appear in the contextual side panel use a UX page property that contains table configurations. To display these tabs for custom tables or case types, create a new UX page property called **contextualTableConfigMapping** and add the table configurations to that property.

The mapping for this property includes the tab name, the table name, and the sys\_id of the table configuration. For example:

```
[{“tab_name”:[{“table=custom_table_name”:”the sys id of the table config”}]},
{“tab_name”:[{“table=custom_table_name”:”the sys id of table config”}]}]

```

```
[{“agent_assist”:[{“table=incident":"e15061a4b30303002bf182c136a8dc34"}]},["response_template":[{“table=template”:”0a73bc83c3041300e2fd5cb981d3ae29”}]}]
```

You can map multiple tables in this property. For example:

```
[{"agent_assist":[{"table=custom_table_name":"the sys id of table config"}, {"table=custom_table_name_2":"the sys id of table config"}]}]
```

You can also use operators to match multiple tables in the property configuration. The operators in the following example include:

-   STARTSWITH
-   ENDSWITH
-   LIKE: This operator is used to match table names with a pattern. In the following example, the LIKE operator would match with all tables that include the word "case".
-   IN: This operator enables you to set a list of values that must match values in your tables.

```
[
  {
    "agent_assist": [
      {
        "tableSTARTSWITHkb_template": "5cb4030e73e2330021741c86fbf6a7e1"
      },
      {
        "tableENDSWITHu_kb_template": "5cb4030e73e2330021741c86fbf6a7e1"
      }
    ],
    "response_template": [
      {
        "tableLIKEcase": "5f0a5f7e77840010ec75945caa1061a5"
      },
      {
        "tableINagent_file, sn_customerservice_case": "82d52b55a300021033d6441d041e61bd"
      }
    ]
  }
]
```

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  Select the **CSM/FSM Configurable Workspace** experience.

3.  In the UX Page Properties related list, select **New**.

4.  Fill in the following fields on the UX Page Property form.

<table id="table_ww1_ptk_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page

</td><td>

CSM/FSM Configurable Workspace

</td></tr><tr><td>

Name

</td><td>

Use this name for the property: **contextualTableConfigMapping**

</td></tr><tr><td>

Type

</td><td>

json

</td></tr><tr><td>

Value

</td><td>

Include an entry for Agent Assist or for Response Template or both.Agent Assist example:

```
[{"agent_assist":[{"table=custom_table_name":"the sys id of table config"}]}]
```

Response Template example:

```
[{"response_template":[{"table=custom_table_name":"the sys id of table config"}]}]
```

Agent Assist and Response Template example:

```
[{"agent_assist":[{"table=custom_table_name":"the sys id of table config"}]},{"response_template":[{"table=custom_table_name":"the sys id of table config"}]}]
```

</td></tr></tbody>
</table>5.  Select **Save**.

    After adding the property, you can open the record page that uses the configured table and test the results in the contextual side panel.


**Related topics**  


[Configuring contextual search](https://www.servicenow.com/docs/access?context=configuring-contextual-search&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

