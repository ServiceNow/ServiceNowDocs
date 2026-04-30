---
title: Issue auto-resolution tab
description: The Issue auto-resolution tab helps you understand how well your Virtual Agent \(VA\) chatbot anticipates user needs. It displays information about the number of user issues intercepted by the auto-resolution service and resolved by VA.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Issue auto-resolution tab

The **Issue auto-resolution** tab helps you understand how well your Virtual Agent \(VA\) chatbot anticipates user needs. It displays information about the number of user issues intercepted by the auto-resolution service and resolved by VA.

Issue auto-resolution takes place when a user is diverted to VA from a non-conversational interface. For example, a user might request a new keyboard through a service portal or email. The auto-resolution service can detect the user request and use VA to resolve the user's request in a VA chatbot session. For more information, see [Auto Resolution for Virtual Agent](auto-resolution-va.md).

The indicators in the **Issue auto-resolution** tab display how well the auto-resolution service is working. This tab is available only when Issue Auto Resolution is enabled and the **Auto Resolution Configuration** record is set as active.

To access the **Issue auto-resolution** tab, you must have the chat analytics admin role or the chat analytics viewer role.

![Data visualizations for this tab include intent and topic-matching results, matching and conversational trends, acceptance rate, and top topics.](../images/issue-auto-resolution-tab-pae.png "Issue auto-resolution tab")

Selecting the data or pointing to the data in the visualizations displays additional information about the data.

<table id="table_sd4_sx5_3pb"><thead><tr><th>

Visualization

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Intents with Matched Topics

</td><td>

Number of intents that match topics enabled for auto-resolution.Select the indicator to view the list of intents that match topics enabled for auto-resolution.

</td></tr><tr><td>

Intents without Matched Topics

</td><td>

Number of intents that don’t have matching topics.Select the indicator to view the list of intents that don’t match topics enabled for auto-resolution.

</td></tr><tr><td>

Intents with Auto-resolution Disabled

</td><td>

Number of intents that match topics not enabled for issue auto-resolution.Select the indicator to view the list of intents that match topics not enabled for auto-resolution.

</td></tr><tr><td>

Intent and topic matching results

</td><td>

Breakdown of incidents by intent matching. For example, incidents with matching intents and topics, and incidents without matching intents.Select the indicator to view the list of incidents with or without matched topics.

</td></tr><tr><td>

Trends in intent and topic matching

</td><td>

Trend showing incidents that have intents with or without matching topics.Select the indicator to view the incidents that have intents with or without matching topics.

</td></tr><tr><td>

Auto resolution conversations

</td><td>

Issue auto-resolution conversations that were resolved or unresolved. Resolved means incidents are in the resolved state after the users interacted with VA.Select the indicator to view the list of conversations that were resolved or unresolved.

</td></tr><tr><td>

Auto resolution conversation trends

</td><td>

Usage trend showing all the issue auto-resolution conversations and how many incidents were successfully resolved.

</td></tr><tr><td>

Issue auto-resolution acceptance rate

</td><td>

Shows the issue auto-resolution notifications that were accepted and declined by users.

</td></tr><tr><td>

Top topics in auto resolution conversations

</td><td>

Frequently used topics in auto resolution conversations. Select the indicator to view the list of topics that are frequently used in auto-resolution conversations.

</td></tr></tbody>
</table>**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)

