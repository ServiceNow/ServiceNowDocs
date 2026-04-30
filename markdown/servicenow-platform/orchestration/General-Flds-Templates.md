---
title: General properties for activity designer templates
description: The following General Property fields are common to all activity designer templates.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# General properties for activity designer templates

The following General Property fields are common to all activity designer templates.

<table id="table_hhs_5nn_cr"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the activity. Select a unique name that makes the activity easily identifiable in the palette. If you do not name the activity, it is identified in the **Data** tab of the Workflow Editor with an index number when it is added to a workflow. This index reflects the order in which the custom activity was added to the workflow. Only custom activities and their output variables appear in the **Data** tab.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the activity does.

</td></tr><tr><td>

Image

</td><td>

Icon that identifies an activity of this type in the workflow palette.

</td></tr><tr><td>

Execution template

</td><td>

Predefined template selected for this activity.

</td></tr><tr><td>

Application

</td><td>

Current [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) set on the instance. To view the scope, click the gear icon on the right side of the title bar in any record or list and look at the value in the **Application** field. The activity runs in this scope within a workflow. You cannot view or change the scope for the instance in the Workflow Editor.

</td></tr><tr><td>

Accessible from

</td><td>

Accessibility setting for this activity, by scope. The following options are available:-   **All application scopes**: This activity is available to all application scopes.
-   **This application scope only**: Use of this activity is restricted to the scope named in the **Application** field.

</td></tr><tr><td>

Category

</td><td>

Category for this activity in the **Custom** and **Packs** tabs. All categories are listed under their scope in the collapsible hierarchy.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the activity.

</td></tr></tbody>
</table>**Parent Topic:**[Create custom activities using custom activity designer templates](../task/create-custom-activities.md)

