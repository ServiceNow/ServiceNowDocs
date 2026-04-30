---
title: Set up script field types in Configurable Workspace
description: Enable your Configurable Workspace to support script field types.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administering forms for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Set up script field types in Configurable Workspace

Enable your Configurable Workspace to support script field types.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Select **Name** for the search value, and enter `script` into the search bar.

    ![Search for script](../image/search_script.png)

3.  Configure the following system properties for the script field.

<table id="choicetable_jlb_wgy_fyb"><thead><tr><th align="left" id="d107471e97">

System property

</th><th align="left" id="d107471e100">

Configuration

</th></tr></thead><tbody><tr><td id="d107471e106">

**glide.ui.workspace.script.code\_editor.enable**

</td><td>

Determines whether to show script fields in forms with a code editor component.

</td></tr><tr><td id="d107471e118">

**glide.ui.workspace.script.code\_editor.autoresize\_line\_limit**

</td><td>

Determines the line number after which the scroll bar should appear for the code editor component.

</td></tr></tbody>
</table>
