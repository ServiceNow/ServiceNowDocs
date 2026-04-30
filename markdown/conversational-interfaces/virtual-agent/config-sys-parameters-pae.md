---
title: System parameter configuration
description: Use system parameters to configure the functionality of the Conversational Analytics dashboard.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Conversational Analytics dashboard reference, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# System parameter configuration

Use system parameters to configure the functionality of the Conversational Analytics dashboard.

Use the following system parameters to configure the functionality of the Conversational Analytics dashboard. You must have the Chat Analytics Admin \[chat\_analytics\_admin\] role.

<table id="table_jsf_frh_k4b"><thead><tr><th>

Functionality

</th><th>

System parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Debug

</td><td>

sn\_ci\_analytics.logging.verbosity

</td><td>

Set this parameter to "debug" to see the debug logs for conversational analytics. The setting makes the logs verbose with debug information.

</td></tr><tr><td>

Reasons

</td><td>

sn\_ci\_analytics.ca.reason\_max

</td><td>

Sets the maximum length of reason strings. The default is 1000 characters.

</td></tr><tr><td>

Hash

</td><td>

sn\_ci\_analytics.show\_hashed\_user\_id

</td><td>

1.  Set this parameter to true to display hashed user Ids on the Conversations and Users pages in the dashboard. The default is false.
2.  Provide read access to Hashed User ID column in the Users \(sys\_user\) table.

</td></tr></tbody>
</table>**Parent Topic:**[Conversational Analytics dashboard reference](conversational-analytics-dashboard-reference-pae.md)

