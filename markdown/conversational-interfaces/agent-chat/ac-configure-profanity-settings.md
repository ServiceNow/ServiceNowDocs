---
title: Configuring Profanity Filter
description: Configure the Profanity Filter for Agent Chat to detect flagged words in the manner that best suits your company's needs.
locale: en-US
release: yokohama
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Agent Chat, Agent Chat, Conversational Interfaces]
---

# Configuring Profanity Filter

Configure the Profanity Filter for Agent Chat to detect flagged words in the manner that best suits your company's needs.

## Before you begin

Role required: admin, virtual\_agent\_admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Chat Settings** &gt; **Agent Chat**.

2.  On the Chat settings card, select **View settings** next to Profanity detection.

3.  On the Profanity detection page, slide the **Active** toggle switch to activate the profanity filter.

4.  In the Choose how to detect flagged words card, configure the settings:

<table id="table_rqd_md4_ndb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use Machine Learning model to detect flagged words

</td><td>

Use model-based mode to determine which words should be marked as flagged words.

</td></tr><tr><td>

Use list of flagged words if no matches are found

</td><td>

Use a keyword-based approach to determine which words should be marked as flagged words. The list of flagged words can be configured on the Flagged Words tab.

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Number of messages before notifying manager

</td><td>

If the number of messages with flagged words that an agent has sent is equal to or exceeds this number within the time threshold, the Profanity Filter sends a message to the manager.

</td></tr><tr><td>

Time threshold \(in hours\)

</td><td>

Number of hours during which the number of messages with flagged words is tracked.

</td></tr></tbody>
</table>5.  On the Flagged Words tab, specify words that the Profanity Filter should flag:

    ![Flagged words tab with sample words.](../image/ci-flagged-words.png)

<table id="table_eqp_4cz_wrb"><tbody><tr><td class="sub-head" colspan="2">

Flagged words

</td></tr><tr><td>

Word

</td><td>

Word that the Profanity Filter should flag.

</td></tr><tr><td>

Keywords

</td><td>

Similar words that the Profanity Filter should also flag.

</td></tr><tr><td>

Allowed

</td><td>

-   **Forbidden** - the word is considered profane and will be flagged.
-   **Allowed** - the word is not considered profane and will not be flagged.


</td></tr><tr><td>

Language

</td><td>

Language that the Profanity Filter applies to.

</td></tr><tr><td>

Status

</td><td>

-   **Active** - if the Profanity Filter detects this word, it will determine whether it is forbidden or allowed.
-   **Inactive** - if the Profanity Filter detects this word, it will not do anything.


</td></tr></tbody>
</table>6.  On the **Agent system messages** tab, configure the messages that the agent might see:

    ![Agent system message tab with sample messages.](../image/agent-system-messages.png)

<table id="table_ojg_scz_wrb"><tbody><tr><td class="sub-head" colspan="2">

Agent system messages

</td></tr><tr><td>

Description

</td><td>

Description of the system message.

</td></tr><tr><td>

Value

</td><td>

Exact wording of the system message that displays to the agent.

</td></tr><tr><td>

Updated

</td><td>

Date and time the message was most recently updated.

</td></tr><tr><td>

Updated by

</td><td>

Name of the user who most recently updated the message.

</td></tr></tbody>
</table>7.  On the **Manager system messages** tab, configure the messages that the manager might see:

    ![Manager system messages tab with sample messages.](../image/manager-system-messages.png)

<table id="table_gry_ycz_wrb"><tbody><tr><td class="sub-head" colspan="2">

Manager system messages

</td></tr><tr><td>

Description

</td><td>

Description of the system message.

</td></tr><tr><td>

Value

</td><td>

Exact wording of the system message that displays to the manager.

</td></tr><tr><td>

Updated

</td><td>

Date and time the message was most recently updated.

</td></tr><tr><td>

Updated by

</td><td>

Name of the user who most recently updated the message.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring Agent Chat](../concept/ci-agent-chat-configuring.md)

