---
title: Debug a Virtual Agent topic
description: Investigate and resolve unexpected behavior in your custom Virtual Agent topics, topic blocks, and controls.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Debug, Virtual Agent, interaction records, topic]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Debug a Virtual Agent topic

Investigate and resolve unexpected behavior in your custom Virtual Agent topics, topic blocks, and controls.

For information about topic discovery issues, see [LLM topic discovery in Virtual Agent](../concept/va-llm.md) and [Resolve Natural Language Understanding \(NLU\) topic discovery issues](va-topic-discovery-issues.md).

## Duplicate a live topic before debugging and changing it

Duplicate a topic rather than update a live topic. The unmodified original topic can serve as both a reference and a backup, and retaining the original enables you to restore the topic quickly. Remember to deactivate the original topic before publishing the duplicate.

## Debug a topic while testing your conversations

As you create or update a topic in Virtual Agent Designer, use the **Test** button in the topic header bar to preview the conversation. The chat test window shows the conversation as it appears within Service Portal. Elements in your conversation might appear differently in third-party messaging applications. Test your conversations in any third-party applications where you intend to deploy Virtual Agent.

The test chat window displays four tabs that provide detailed information for debugging and refining your topic: **Analyze test phrases**, **Variables**, **Context**, and **Logs**. For details on these tabs, see [Testing NLU/Keyword topics](va-designer-testing.md). The following example shows the processing messages and errors logged during testing.

![Conversation preview logs shown in the topic preview window.](../images/va-conv-preview-logs2.png)

## Watch for warnings on controls within your topic

![Number of warnings shown in red on the canvas and on the individual controls. For the Text User Input control, Node Name and Prompt are mandatory](../images/va-control-warning.png "Warnings on a topic node in the Flow tab")

Controls that are missing necessary information show a red incomplete badge in the upper left corner of the control. The badge shows a number indicating the number of issues in that control. Select this badge to see a list of the issues in the control.

Another warning badge appears in the upper left corner of the canvas to indicate the number of issues within the entire topic.

## Check for errors when a topic preview does not run

![The topic validator window giving a preview of errors on the canvas.](../images/va-validator.png "Topic preview errors on the canvas")

Additional information appears in a Validation Issues tab on the sidebar of the Virtual Agent Designer canvas when an error prevents the topic from running. The total number of Issues are listed, along with details and a hyperlink for each node. Select a hyperlink to go to the node, and use the information provided to correct any errors in your conversation. You can close the tab without correcting the issues, but until the issues are corrected, the Validation Issues tab appears when you select **Publish**. The Validation Issues tab closes if you select **Publish** after correcting all issues.

## Common Virtual Agent issues

<table id="table_j3r_2jz_12b"><thead><tr><th>

Issue

</th><th>

Possible resolution

</th></tr></thead><tbody><tr><td>

Cannot see module designer under conversational interfaces

</td><td>

-   User might not have the virtual\_agent\_admin role.
-   Virtual Agent plugin might not be activated.

</td></tr><tr><td>

Cannot edit a topic

</td><td>

Logged-in user must be in the same application scope as the topic.

</td></tr><tr><td>

Cannot preview topic

</td><td>

-   Make sure that all required fields are filled in on the node properties.
-   Ensure that your browser is configured to permit pop-ups from your instance.

</td></tr><tr><td>

chat widget stuck at Connecting...

</td><td>

One or more of your topics might be missing. Check the to ensure that topics are present on the instance and in the Active state.

</td></tr></tbody>
</table>## Review topics that run in a conversation flow

Each Virtual Agent \(VA\) conversation in an instance automatically generates an interaction record in the Interactions \[interactions\] table, which logs the conversation between a requester and virtual and live agent. You can review the transcript of the conversation between the requester and virtual agent, including live agent transfers \(if using Agent Chat\). For details, see [Virtual Agent interaction records](../concept/va-interactions.md).

-   **[Resolve Natural Language Understanding \(NLU\) topic discovery issues](va-topic-discovery-issues.md)**  
If an intent is not being chosen when expected, you can troubleshoot NLU prediction errors.
-   **[Natural Language Understanding topic discovery logic in Virtual Agent](../concept/how-topic-discovery-works.md)**  
Understand how Virtual Agent returns intents and how it selects which intents to show to the user.

**Parent Topic:**[Getting started with Virtual Agent Designer](conversation-designer-virtual-agent.md)

