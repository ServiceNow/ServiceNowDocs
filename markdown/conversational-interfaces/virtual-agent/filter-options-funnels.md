---
title: Legacy - Filter options in funnels
description: Use filter options for creating steps in funnels. You can create steps in funnels for cumulative filtering of a conversation flow.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Funnels tab, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Filter options in funnels

Use filter options for creating steps in funnels. You can create steps in funnels for cumulative filtering of a conversation flow.

## Overview of filter options

You can define each step depending on your data of interest in the conversation flow. For more information, see [Funnels tab](../concept/funnels-tab.md).

A step consists of the following:

-   Field: The item on which the step is evaluated.
-   Operator: A list of operators that is contextually generated based on the selected field.
-   Value: A text entry field or a list that is contextually generated based on the selected field.

The field options are listed in the following table:

<table id="table_owp_3hn_wnb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conversation start \(1st\)

</td><td>

New users who had a conversation with Virtual Agent.

</td></tr><tr><td>

Conversation start \(Any\)

</td><td>

All users who had conversations with Virtual Agent. This option includes all users regardless of the number of times the users have interacted with Virtual Agent.

</td></tr><tr><td>

Events

</td><td>

Events that are triggered in a conversation.

</td></tr><tr><td>

Topic

</td><td>

List of all topics that were used in the conversation flow. The list of topics can be refined further to these topic types:-   Setup topics: List of topics that provide basic conversational flows such as the conversation greeting or closing.
-   Standard topics: List of topics only and not topic blocks or pre-built topics.
-   Topic blocks: List of topic blocks only.

**Note:** When a funnel contains topics that were modified, for example, nodes were added or removed, after the funnel was created, the funnel does not consider those changes. You have to create a new funnel to account for those changes.

</td></tr></tbody>
</table>**Parent Topic:**[Funnels tab](../concept/funnels-tab.md)

