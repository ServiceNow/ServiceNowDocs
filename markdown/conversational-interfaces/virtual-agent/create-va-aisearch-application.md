---
title: Create a custom AI Search experience for Virtual Agent conversations
description: Define a custom AI Search experience in a conversation using the AI Search topic block. You create a Search Application Configuration used by the topic block to control the AI Search results returned in the conversation. Or you can use the Search Application Configuration to control AI Search results in a custom chat experience.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Improving the user experience with AI Search, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a custom AI Search experience for Virtual Agent conversations

Define a custom AI Search experience in a conversation using the AI Search topic block. You create a Search Application Configuration used by the topic block to control the AI Search results returned in the conversation. Or you can use the Search Application Configuration to control AI Search results in a custom chat experience.

## Before you begin

Create the search profile that defines the search experience to be used in the search application configuration. For details, see Search profiles and Search application configurations.

Role required: virtual\_agent\_admin or admin with the search application administrator \[search\_application\_admin\] role

## About this task

A search application configuration specifies the AI Search profile used by the Run AI Search topic block or in a custom chat experience to control the search experience, such as the search source used to generate search results.

**Note:** As of the Utah release, use the AI Search topic block when creating an AI Search application. \(The Run AI Search topic block is used in releases from Rome to Tokyo.\)

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications** and select **New** to create the search application configuration.

2.  On the form, fill in the fields.

    For more information, see Search Application Configuration form.

3.  Select **Submit**.

4.  Apply the custom Search Application Configuration to the AI Search topic block used in a conversation or to a custom chat experience.

<table id="choicetable_csd_xws_wqb"><thead><tr><th align="left" id="d81512e171">

Option

</th><th align="left" id="d81512e174">

Procedure

</th></tr></thead><tbody><tr><td id="d81512e180">

**Specify the custom Search Application Configuration in the AI Search topic block used in a conversation**

</td><td>

Add the AI Search topic block to a conversation topic. For details, see [Add a reusable topic block to a calling topic or topic block](add-topic-blocks-to-topic.md).1.  Navigate to **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer** and select the topic or [create a new topic](create-virtual-agent-topic.md).
2.  In the Flow tab, drag the Topic Block utility onto the canvas.
3.  Complete the Topic Block Properties sheet:
    -   In the **Topic Block** field, select AI Search.
    -   In the **Search Term \(String\)** field, use dot-walking or a script to specify the input variable for the search.
    -   In the **Search Application Configuration** field, select the custom Search Application Configuration that you created in a previous step.

If you leave this field empty, AI Search uses the default search application configuration for Virtual Agent.

    -   If needed, click **Hide this node** and specify conditions.
4.  Select **Save**.

The AI Search topic block runs the selected search application configuration to generate the customized AI Search experience.

</td></tr><tr><td id="d81512e290">

**Use the custom Search Application Configuration in a custom chat experience**

</td><td>

Create or update a custom chat experience that uses the Run AI Search topic block with the custom Search Application Configuration. For details on creating a custom experience, see [Configure a Virtual Agent chat experience](configure-default-chat-experience.md).

</td></tr></tbody>
</table>    Your custom Search Application Configuration is used in the AI Search topic block in a conversation or a custom chat experience to generate the customized AI Search experience.


**Parent Topic:**[Improving the user experience with AI Search](../concept/va-ai-search.md)

