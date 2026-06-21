---
title: Set up script field types in Configurable Workspace
description: Enable your Configurable Workspace to support script field types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-user-interface/configure-user-experiences/use-script-field-types-in-your-configurable-workspace.html
release: yokohama
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-01-30"
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

    \[Omitted image "search\_script.png"\] Alt text: Search for script

3.  Configure the following system properties for the script field.

<table id="choicetable_jlb_wgy_fyb"><thead><tr><th align="left" id="d74253e97">

System property

</th><th align="left" id="d74253e100">

Configuration

</th></tr></thead><tbody><tr><td id="d74253e106">

**glide.ui.workspace.script.code\_editor.enable**

</td><td>

Determines whether to show script fields in forms with a code editor component.

</td></tr><tr><td id="d74253e118">

**glide.ui.workspace.script.code\_editor.autoresize\_line\_limit**

</td><td>

Determines the line number after which the scroll bar should appear for the code editor component.

</td></tr></tbody>
</table>
