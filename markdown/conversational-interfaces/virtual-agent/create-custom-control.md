---
title: Create a Virtual Agent custom control
description: Build a custom input or response control that topic authors can use in topics or topic blocks. In Virtual Agent conversations, an input control gathers information from end users, while a response control displays information to end users.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Virtual Agent, custom control, custom input, response control]
breadcrumb: [Customizing Virtual Agent with custom controls, Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent custom control

Build a custom input or response control that topic authors can use in topics or topic blocks. In Virtual Agent conversations, an input control gathers information from end users, while a response control displays information to end users.

## Before you begin

[Create the custom control definition](create-custom-control-definition.md).

**Important:** To implement secure \(password2\) inputs in your Virtual Agent custom control, you must adhere to the scoped application requirements in Workflow Studio. For details, see [Workflow Studio scoped application requirements for secure inputs](../concept/va-fd-app-reqs-secure-inputs.md).

**Tip:** Developers and topic authors may need to access custom controls created in other application scopes. To give them access, see [Create cross-scope access privileges for topic blocks and custom controls](configure-cross-scope-privileges.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the home page, select **Create.**

3.  On the form, fill in the fields.

<table id="table_dzy_15h_cmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

List of assets that you can create in Virtual Agent Designer.

 Choose the type of custom control:

-   **Custom Input Control**
-   **Custom Response Control**


</td></tr><tr><td>

Name

</td><td>

Unique name for the custom control that reflects its purpose.

</td></tr><tr><td>

Description

</td><td>

Brief explanation of the purpose and functionality of the control.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced properties \(optional\)

</td></tr><tr><td class="sub-head" colspan="2">

Make inputs secure\[Custom input controls only\]

</td></tr><tr><td>

Enable

</td><td>

Toggle switch that lets a custom input control pass secure inputs, such as passwords.

</td></tr><tr><td class="sub-head" colspan="2">

Available on the palette

</td></tr><tr><td>

Enable

</td><td>

Toggle switch that determines whether the custom control appears as its own icon in the Utilities section of the palette on the **Flow** tab. This provides easy access to the control for other authors.

</td></tr><tr><td class="sub-head" colspan="2">

Additional

</td></tr><tr><td>

Categories

</td><td>

List of categories. Categories identify and group related topics, topic blocks, or custom controls. If applicable, choose a category for your control.

</td></tr></tbody>
</table>4.  Select **Create**.

    The **Flow** tab opens and displays an initial flow that contains a custom control node.

5.  Select the **Start** node and define the input parameters to the control.

    Topic authors will provide these input parameters and values from the calling topic.

    1.  Select **+ Add**.

    2.  On the form, fill in the fields.

<table id="id_n4c_4sz_gpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the input variable that stores the input value.

</td></tr><tr><td>

Type

</td><td>

Type of data being passed to the topic block. For example, **String**, **Boolean**, and so on. The fields change according to your choice. For more information, see [Input data types in Virtual Agent topics](../reference/va-data-types.md).

</td></tr><tr><td>

Required

</td><td>

Option to set the parameter as required.

</td></tr><tr><td>

Hint

</td><td>

Tooltip that is visible when authoring a calling topic. See the following example:![Input variable mapping tooltip in this example displaying "Test Hint String."](../images/va-topic-block-hint.png)

</td></tr><tr><td>

Table

</td><td>

ServiceNow table that is used to query for input.This field is available only when **Reference** or **Array.Reference** is selected from the **Type** field.

</td></tr><tr><td>

Max Number of Rows

</td><td>

Maximum number of rows that the topic block is allowed to define.This field is available only when **Array** is selected from the **Type** field.

</td></tr><tr><td>

Default Value

</td><td>

Default value for the variable. This value can be used when previewing the block.Duplicate default values are not allowed for array data types.

</td></tr></tbody>
</table>    3.  Select **Save**.

    4.  Repeat these steps for additional parameters.

6.  Select the **End** node and define the output parameters and values returned from the custom control.

    Topic authors can use the output value in the calling topic.

    1.  Select **+ Add New**.

    2.  Enter the name and value of the parameter.

    3.  Repeat these steps for additional parameters.

    4.  Select **Save**.

7.  Select the custom control node and complete the property sheet as follows:

    -   For a custom input control, fill in the [Custom input properties sheet](../reference/custom-input-properties-form.md).
    -   For a secure custom input control, fill in the [Secure custom input properties sheet](../reference/secure-custom-input-properties-form.md).
    -   For a custom response control, fill in the [Custom output properties sheet](../reference/custom-response-properties-form.md).
8.  To create the control, select **Save** and then **Publish**.


## Result

If you selected **Available on the palette** in the Properties page, the Custom Control icon displays as its own icon in the Utilities section of the palette. The control is listed on the Topics page, and you can use the Type menu to show only custom controls.

## What to do next

[Add a custom control to a Virtual Agent topic or topic block](embed-custom-control.md).

