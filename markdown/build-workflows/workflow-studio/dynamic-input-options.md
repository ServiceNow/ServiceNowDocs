---
title: Dynamic input configuration options
description: Use these options to configure dynamic inputs.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Dynamic inputs, Create an action in Workflow Studio, Building actions, Use, Workflow Studio, Build workflows]
---

# Dynamic input configuration options

Use these options to configure dynamic inputs.

## Common input options

<table id="table_rh5_myr_tgb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Enter a label that appears for the action input when the action is added to a flow.

</td></tr><tr><td>

Name

</td><td>

Enter a name used to refer to the input in system records and in scripts.

</td></tr><tr><td>

Type

</td><td>

Select one of the dynamic data types.-   Dynamic Choice
-   Dynamic Inputs
-   Dynamic Template

</td></tr></tbody>
</table>## Dynamic Choice advanced options

<table id="table_v3w_552_gxb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name used to refer to the input in system records and in scripts.

</td></tr><tr><td>

Default Value

</td><td>

Enter a string value to use as a default for choice list.

</td></tr><tr><td>

Max length

</td><td>

Enter the maximum character length for one choice or template field value.

</td></tr><tr><td>

Hint

</td><td>

Enter a hint to display for the choice list.

</td></tr><tr><td>

Choice

</td><td>

Select one of the following choice list options: -   **Dropdown with --None--**
-   **Dropdown without --None--**

</td></tr><tr><td>

Action

</td><td>

Select the data gathering action to generate choice list values. For example, an action that converts records into a choice list options.

</td></tr></tbody>
</table>## Dynamic Inputs advanced options

|Option|Description|
|------|-----------|
|Action|Select the data gathering action to generate additional action inputs. For example, an action that converts Service Catalog variables into additional action inputs.|

## Dynamic Template advanced options

|Option|Description|
|------|-----------|
|Hint|Enter a hint to display for the record whose fields you want to dynamically display.|
|Default Value|Select a field and field value to use as a default for the action.|
|Action|Select the data gathering action to generate record template values. For example, an action that displays the fields of a third-party record or service.|

**Parent Topic:**[Dynamic inputs](../concept/dynamic-inputs.md)

**Related topics**  


[Get started with dynamic inputs](../task/getting-started-dynamic-input.md#)

[Create a data gathering action for a dynamic choice](../task/create-data-gathering-action-dynamic-choice.md)

[Create a data gathering action for a dynamic template](../task/create-data-gathering-action-dynamic-template.md)

[Create a data gathering action for a dynamic inputs type input](../task/create-data-gathering-action-dynamic-inputs.md)

