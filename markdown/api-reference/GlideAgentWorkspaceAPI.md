---
title: GlideAgentWorkspace \(g\_aw\) - Client
description: The g\_aw API provides methods that enable a UI action or client script to open a specified record in an Agent Workspace tab.Closes the currently open record, such as a form, in a subtab within Agent Workspace.Opens a specified record, such as a form, in a subtab within Agent Workspace.
locale: en-US
release: xanadu
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideAgentWorkspace \(g\_aw\)- Client

The g\_aw API provides methods that enable a UI action or client script to open a specified record in an Agent Workspace tab.

There is no constructor for this class. Access GlideAgentWorkspace methods using the `g_aw` global object.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideAgentWorkspace - closeRecord\(\)

Closes the currently open record, such as a form, in a subtab within Agent Workspace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example saves the content of the tab and then closes it.

```
function onClick(g_form) {
```

```
function onClick(g_form) {
  g_form.save().then(function(){
    g_aw.closeRecord();
  });
}
```

## GlideAgentWorkspace - openRecord\(String table, String sysId, Object params\)

Opens a specified record, such as a form, in a subtab within Agent Workspace.

**Note:** This method is only available in the Agent Workspace client scripting environment or in a UI action on the workspace client script field.

<table id="table_lhq_mph_bhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

table

</td><td>

String

</td><td>

Name of the table that contains the record to open.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td>

Sys ID of the record to open.

</td></tr><tr><td>

params

</td><td>

Object

</td><td>

Optional. Name/value pairs of the parameters to pass to the record.```
"params": {
  "readOnlyForm": Boolean;
  "defaultTab": "String";
  "hideDetails": Boolean
}
```

</td></tr><tr><td>

params.readOnlyForm

</td><td>

Boolean

</td><td>

Flag that indicates whether all fields on the opened record are read-only; regardless of the UI policy and ACLs.-   true: All fields are read only.
-   false: Fields adhere to the associated UI policy and ACLs.

 Default: false

</td></tr><tr><td>

params.defaultTab

</td><td>

String

</td><td>

Name of the initial tab to display in the workspace. You can only specify related items or related lists.If not specified, the details tab appears unless **hideDetails** is set to true.

 For more information on the method to use to obtain a related list name, see [getRelatedListNames\(\)](../../GlideForm/concept/c_GlideFormAPI.md#).

</td></tr><tr><td>

params.hideDetails

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the details tab and the UI actions.-   true: Only the form header, all other tabs, and the first available tab appear on the form.
-   false: Details tab and UI actions appear on the form.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

Open a sys\_user record in a subtab.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1'); 
```

Open a record in a subtab where all fields are read-only.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1', {readOnlyForm: true}); 
```

Open a record in a subtab and go directly to the "Groups" related list.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1', {defaultTab: "sys_user_grmember.user"});  
```

Open a record in a subtab but only show the form header and other tabs.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1', {hideDetails: true}); 
```

