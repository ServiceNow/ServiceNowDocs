---
title: Create the Asset Refresh topic in Virtual Agent Designer
description: Create the topic in Virtual Agent Designer using topic blocks that come with the ITSM Virtual Agent Conversations plugin. When the user receives a notification that it's time to upgrade, they will be directed to this topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [Asset, Refresh, Topic, Virtual Agent, Designer, ITSM, Conversations, plugin, com.glide.cs.chatbot, NLU, Natural Language Undersatnding]
breadcrumb: [Example Asset Refresh Virtual Agent conversation with notifications, Virtual Agent chat widget interface for NLU, Explore, Virtual Agent, Conversational Interfaces]
---

# Create the Asset Refresh topic in Virtual Agent Designer

Create the topic in Virtual Agent Designer using topic blocks that come with the ITSM Virtual Agent Conversations plugin. When the user receives a notification that it's time to upgrade, they will be directed to this topic.

## Before you begin

Install the following applications:

-   Glide Virtual Agent plugin \(com.glide.cs.chatbot\)

    You must have a subscription for Virtual Agent before you can activate the Glide Virtual Agent plugin.

-   [Enable Natural Language Understanding \(NLU\)](configure-nlu-settings.md), if not already enabled \(recommended\).
-   ITSM Virtual Agent Conversations \(available in the ServiceNow® Store\)

    If this application is already installed, check the ServiceNow Store for an updated version before you begin.


Determine the application scope for your Virtual Agent topic and actionable notification. They don't have to reside in the same application scope, but it can be easier to maintain if they do.

Publish the following ITSM Virtual Agent components. If you're using an application scope other than ITSM Virtual Agent Conversations, you should duplicate and publish these topic blocks in the scope you intend to use. To do this, change your application scope, and then duplicate the topic blocks in Virtual Agent Designer.

-   Create Incident topic block
-   Request Catalog Item topic block
-   AI Search topic block
-   Search Catalog Item topic block

Role required: virtual\_agent\_admin or admin

## About this task

For more information about building topics and the Virtual Agent Designer interface, see the following topics:

-   [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)
-   [Creating a Virtual Agent topic](create-virtual-agent-topic.md)
-   [Assistant Designer controls](../concept/virtual-agent-controls.md)
-   [Assistant Designer interface reference](../concept/vad-reference.md)

**Tip:** Look through existing conversations to ensure you are not duplicating effort, and familiarize yourself with Virtual Agent and the flow of topics. Additionally, it may be helpful to outline the flow of a conversation before building it in Virtual Agent Designer.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the Topics page, select **Create**.

    ![Virtual Agent Designer +Create tile on the landing page.](../images/vad-create-tile.png)

3.  On the Create a topic form, set up your topic.

    1.  Enter a name, such as `Asset Refresh`.

    2.  If NLU is enabled, select an existing model, or create a new one.

    3.  Select or create an intent for the NLU model.

        ![In the Associated Intent field, select an existing intent or create a new one for your topic.](../images/example-create-intent-vad.png)

        For descriptions of all field values, see [Create a topic form](../reference/vad-topic-creation-form.md).

    4.  Select **Create**.

    The **Flow** tab appears with Start and End nodes. For an overview of this screen and its components, see [Topic Flow tab](../reference/vad-topic-flow-tab.md).

4.  Create your initial message to greet the user.

    1.  From the Components area, drag a Text bot response node onto the canvas.

    2.  Select the node to view the properties palette.

    3.  Enter a name for the node and the response you want to display to the user.

        ![Enter a unique node name, such as Initial Message. Include a response, such as "You're eligible to upgrade!"](../images/example-topic-text-response.png)

5.  Ask the user if they want to proceed with the asset refresh.

    1.  From the Components area, drag a Static choice input node onto the canvas.

    2.  In the properties palette, enter the following information:

        -   A unique name, such as `Continue or Defer`.
        -   A text prompt, such as `What would you like to do next? Learn more, or continue with the upgrade?`
        -   In the Choices area, provide a text prompt for each choice and a value for that choice, so you can refer to it later on.

            For example, your choices might be `Learn more` and `Continue with upgrade`. The values should make sense as variable names. For example, `info` and `upgrade`.

    ![Static choice properties for "Continue or Defer" node. It includes a user prompt and two choices: Learn more or Continue with upgrade.](../images/example-static-choice-continue.png)

6.  Add a Decision utility to handle the user's choice.

    1.  From the Components area, drag a Decision utility onto the canvas.

    2.  Select the plus icon to add a second branch.

    3.  Name each branch to correspond with the decisions \(info and upgrade\).

        ![This Decision utility has two branches: info and upgrade. They are based on the choices offered to the user in the previous step.](../images/continue-or-defer-decision.png)

    4.  For each branch, select it and then use the Branch Condition area to indicate which option the branch will follow.

        ![Use the condition builder to specify the Continue or Defer choice node and the corresponding user choice that this branch will follow, such as "Continue with upgrade."](../images/continue-defer-decision-condition.png)

7.  For the upgrade branch, add a Lookup utility node to confirm that the user still has the asset.

    1.  From the Components area, drag a Lookup utility onto the canvas.

        ![Drag the Lookup utility node onto the upgrade path on the canvas.](../images/crawl-ex-lookup-canvas.png)

    2.  In the properties palette, specify the following information:

        -   A unique name, such as `Asset Lookup`.
        -   The table name: **Asset \[alm\_asset\]**
        -   In the Condition builder, select **Assigned to**, and then dot-walk to **Input Variables &gt; User**. Select **and** to include **State &gt; is &gt; In maintenance**.

            The asset state will tie into the notification you send the user for this asset refresh.

            ![Filter assets in the Assign Condition builder using Assigned to is the current user, and the State is In maintenance.](../images/crawl-ex-lookup-condition.png)

8.  Ask the user if they still have the asset.

    1.  From the Components area, drag a Boolean input node onto the canvas.

        The Boolean node automatically asks if you want to add a Decision utility with two paths. Select **Yes**. A Decision node appears in the flow with values of **true** and **false**. Both are already mapped to the Boolean node.

    2.  Add a user prompt.

        Use dot-walking to refer to the asset found by the Asset Lookup node.

        ![Write a prompt, such as "Do you still have this device?" Then dot-walk to Input Variables > Asset Lookup > Display name.](../images/crawl-ex-boolean-dotwalking.png)

9.  If the user still has the asset \(the Boolean response is **true**\), we want to search for it in the catalog.

    1.  From the Components area, drag the Topic Block utility onto the Asset Check **true** branch on the canvas.

    2.  In the properties palette, select **Search Catalog Item** for the Topic block.

    3.  Under Input mapping, use dot-walking to specify the **query\_term** parameter from the Asset Lookup node \(Input Variables &gt; Asset Lookup &gt; Display name\).

    The catalog search will provide these output variables by default, shown under Output mapping.

    ![Output mapping variables for Search Catalog Item are the catalog_item_id, item_type, and is_conversational.](../images/crawl-ex-search-output-vars.png)

10. Request the upgraded item.

    1.  From the Components area, drag the Topic Block utility onto the canvas beneath the Search Catalog Item topic block.

    2.  In the properties palette, select **Request Catalog Item** for the Topic block.

    3.  In the Input mapping area, use dot-walking to specify the **catalog\_item\_id** that the previous topic block returned.

        ![For the catalog_item_id field, select the dot-walking icon and choose Input Variables > Catalog_item_id.](../images/crawl-ex-req-catalog-item.png)

    This topic block returns output variables as well. The user will be able to select variables for their new device, as well. You can configure these variables in Service Catalog.

11. Ask the user to confirm their choice of device.

    1.  From the Components area, drag the Card bot response node onto the canvas beneath the Request Catalog Item topic block.

    2.  In the properties palette, specify the following information:

        -   A unique name, such as `Device Request Record`.
        -   Card type: **Record**
        -   Populate this card by referencing: **Table**
        -   Table name: **Requested Item \[sc\_req\_item\]**
        -   In the Condition builder, add **Sys ID is Input Variables&gt;Record\_id**.

            ![In the Assign Condition builder, select Sys ID, then is. For the third field, dot-walk to Input Variables > Record_id.](../images/crawl-ex-sysid-is-record-id.png)

        -   In the **fields** area, select the record columns to display in the card to the user.

            For example, specify **Number**, **Short description**, and **Estimated delivery**.

12. Drag this flow's arrow to the End node to complete this part of the workflow.

    ![Drag the flow arrow that follows the Device Request Record node to the End node. This signals the end of the topic for this particular flow.](../images/crawl-ex-drag-arrow-end.png)

13. Select **Save**.


## What to do next

[Create the Open Incident workflow in the Asset Refresh topic](create-example-asset-refresh-flow2.md)

**Related topics**  


[Maximizing code reuse with topic blocks](../concept/topic-blocks-overview.md)

