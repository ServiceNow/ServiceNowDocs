---
title: Add a reusable topic block to a calling topic or topic block
description: Add a reusable topic block to a calling \(parent\) topic or topic block to run a specific function or task in the calling topic. You specify input parameters used in the topic block, and you specify output parameters that are used by the calling topic.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Maximizing code reuse with topic blocks, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Add a reusable topic block to a calling topic or topic block

Add a reusable topic block to a calling \(parent\) topic or topic block to run a specific function or task in the calling topic. You specify input parameters used in the topic block, and you specify output parameters that are used by the calling topic.

## Before you begin

Review the topic blocks available on the home page in Virtual Agent. You can [create a new topic block](create-topic-blocks.md). You can also use a pre-built topic block, duplicate it, and customize it. Pre-built topic blocks are installed automatically with the Glide Virtual Agent plugin, as well as the [Virtual Agent conversation plugins](../reference/prebuilt-topics-ITSM.md#table_rmj_1s5_mhb) for Customer Service Management, HR Service Delivery, and ITSM.

Verify that the topic block you want to use is published and active.

Role required: virtual\_agent\_admin or admin

## About this task

You can specify the following types of variables:

-   Input variables that are passed to the topic block.
-   Output variables that are returned from the topic block to the calling topic.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the home page, select the calling topic or topic block in which you will include the topic block.

    The **Flow** tab displays the conversation flow.

3.  Depending on the type of topic block you are adding, add the appropriate Virtual Agent controls \(nodes\) to the conversation.

    For example, if you are adding the Contextual Search topic block, you could add the Text user input control to request an item from the user. Drag that control before the node for the Contextual Search topic block.

4.  From the Utilities section of the palette, drag the Topic Block control onto the canvas at the appropriate location in the conversation flow.

5.  In the Topic Block properties sheet, select the name of the topic block that you want to add.

    The property sheet for the selected topic block displays the input and output parameters. The name of the selected topic block automatically pre-populates the **Node name** field. You can override the name if needed.

6.  Set the required Input Mapping variables and, if applicable, the Output Mapping variables for the selected topic block.

7.  In the header bar, select **Save**.

8.  To preview your calling topic, select **Test** in the header bar.

    You can see how the calling topic runs in the chat window.

    If the Now Assist panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Now Assist panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments.

9.  If no further changes are needed, select **Publish** in the header bar.


