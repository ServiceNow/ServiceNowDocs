---
title: Create a reusable topic block
description: Build a reusable component that performs a specific subflow of tasks and conversational elements in Virtual Agent conversations.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
keywords: [Reusable, Topic, Block, Virtual Agent, subflow, conversations]
breadcrumb: [Maximizing code reuse with topic blocks, Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create a reusable topic block

Build a reusable component that performs a specific subflow of tasks and conversational elements in Virtual Agent conversations.

## Before you begin

**Tip:** Developers and topic authors may need to access topic blocks created in other application scopes. To give them access, see [Create cross-scope access privileges for topic blocks and custom controls](configure-cross-scope-privileges.md).

Role required: virtual\_agent\_admin or admin

## About this task

Use topic blocks to run common steps, such as retrieving certain records.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the home page, do one of the following:

    -   To create a topic block from scratch, select **Create**.
    -   To create a topic block based on a pre-built topic block, open the topic block and do the following:
        1.  In the header bar, select **Duplicate**.
        2.  Enter the name of the new block and select **Save**.
3.  On the sheet, fill in the fields.

<table id="table_jlp_q1z_njb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

List of items that you can create in Virtual Agent Designer.

 Select **Topic Block** and define the additional properties.

**Note:** Once you set this topic as a topic block, you cannot change it to a regular topic.

</td></tr><tr><td>

Name

</td><td>

Unique name for the topic block that reflects its functional purpose. This name appears in the list of topic blocks that topic authors can choose from when creating or updating a topic.

</td></tr><tr><td>

Description

</td><td>

Brief explanation of the purpose of the topic block. For example, to retrieve records.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced properties \(optional\)

</td></tr><tr><td class="sub-head" colspan="2">

Who can access this topic

</td></tr><tr><td>

Channels

</td><td>

Chat clients in which the topic or topic block will run.

 These channels are different from the default channels that are natively supported by Virtual Agent. Your instance may have additional channels for [custom chat integrations](../concept/va-custom-adapter-framework.md) created for it. For more information about channels, see [Deploying Virtual Agent topics in other channels](../concept/va-integrations.md).

</td></tr><tr><td class="sub-head" colspan="2">

Live agent

</td></tr><tr><td>

Live agent context variables

</td><td>

Live agent context variables that are defined in the [General Chat Settings](../../conversational-interfaces/task/ac-configure-context-variables.md).Select the variables that provide dynamic context, which means information from the Virtual Agent chat. This information is transferred from the bot conversation to the live agent.

For information about the default list of live agent variables, see [Live agent chat context variables](../reference/live-agent-chat-context-vars.md).

</td></tr><tr><td>

Available for Agent Autopilot

</td><td>

Toggle switch that determines whether the topic block is available to a live agent.When enabled, an agent can search for the topic and invoke the topic. For details, see [Conversation Autopilot](../../conversational-interfaces/concept/ci-agent-chat-using.md#).

</td></tr><tr><td class="sub-head" colspan="2">

Available on the palette

</td></tr><tr><td>

Enable

</td><td>

Toggle switch that determines whether the topic block appears as its own icon in the Utilities section of the palette on the **Flow** tab. This provides easy access to the topic block for other authors.

</td></tr><tr><td class="sub-head" colspan="2">

Additional

</td></tr><tr><td>

Categories

</td><td>

Category that contains this block. You can define [custom topic categories](create-topic-category.md) for your topic blocks.

</td></tr></tbody>
</table>4.  Select **Create**.

    The **Flow** tab opens. The canvas displays a flow with a **Start** and **End** node.

5.  To define an input to the block, do the following:

    1.  Select the **Start** node in the canvas.

    2.  In the Start Segment Properties sheet, select **+ Add**

    3.  On the sheet, fill in the fields.

<table id="id_w2q_ksz_gpb"><thead><tr><th>

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
</table>        For example, the pre-built Contextual Search topic block provides the following input parameters:

        ![Input parameters for the Contextual Search topic block include context, query, portal, and kb_knowledge_base.](../images/TopicBlockStartSegment.png)

    4.  Select **Save**.

    The calling topic or topic block passes input parameters to the topic block.

6.  Drag Virtual Agent Designer controls onto the canvas.

    These controls include the input, bot responses, and utilities. Use them in combination to define the logic that is run in the topic block. For more information, see [Virtual Agent Designer controls](../concept/virtual-agent-controls.md).

7.  To define the output returned from the topic block, do the following:

    1.  Select the **End** node in the canvas.

    2.  In the End Segment Properties sheet, select **+ Add New**.

    3.  On the sheet, fill in the following fields.

        -   **Name**: Name of the value returned from the topic block.
        -   **Value**: Either a string with variables or a script that can be used within the calling topic. The **Value** is presented as data pills for the input variables that you defined \(the **Default Value** specified in the Input Parameters and the input values from the node in the topic block\).
        For example, the pre-built Contextual Search topic block passes the following output parameters:

        ![Output parameters for the Contextual Search topic block include Results returned and Results Helpful.](../images/TopicBlockEndSegment.png)

    4.  Select **Save**.

    When the topic block finishes running in the calling topic, it can pass output variables to the calling topic.

8.  To see how the topic block runs, select **Test**.

    For example, the Contextual Search topic block returned the following results, including a preview-only message with the output values. The preview message helps you verify expected outputs and is not viewable to your users.

    ![The preview window displays the chat conversation and a preview only section that shows the output variables and their values. For example, "results_helpful":true.](../images/preview-topic-block.png)

9.  If you're ready to make the topic block available for use in calling topics, then do the following:

    1.  Remove the default parameters that you used for testing.

    2.  Select **Save**, and then select **Publish**.

    The topic block state changes to Active and is ready for use in calling topics.


## What to do next

[Add a reusable topic block to a calling topic or topic block](add-topic-blocks-to-topic.md).

