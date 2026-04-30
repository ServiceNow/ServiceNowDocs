---
title: System property configuration
description: Use system properties to configure the functionality of the Conversational Analytics dashboard.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Conversational Analytics dashboard reference, Conversational Analytics dashboard, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# System property configuration

Use system properties to configure the functionality of the Conversational Analytics dashboard.

Use the following system properties to configure the functionality of the Conversational Analytics dashboard. You must have the Chat Analytics Admin \[chat\_analytics\_admin\] role.

<table id="table_jsf_frh_k4b"><thead><tr><th>

Functionality

</th><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Debug

</td><td>

sn\_ci\_analytics.logging.verbosity

</td><td>

Set the value of this property to "debug" to see the debug logs for conversational analytics. The setting makes the logs verbose with debug information.

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

1.  Set the value of this property to true to display hashed user Ids on the Conversations and Users pages in the dashboard. The default is false.
2.  Provide read access to Hashed User ID column in the Users \(sys\_user\) table.

</td></tr><tr><td>

Max search breakdown

</td><td>

sn\_ci\_analytics.max.search.threshold

</td><td>

Sets the maximum breakdown elements for search. Default value is 10000. The value of this property should not exceed 10000. Use this property in conjunction with the properties in Performance Analytics.**Note:**

If the data on User Search Metrics page does not load due to an invalid configuration error, set the value of com.snc.pa.scorecards.max\_breakdown\_elements property to 10000. The default value of this property is 1000.

If the number of search terms exceeds the limit specified in the com.snc.pa.dc.max\_breakdown\_elements\_limit property, the dashboard will not show any data. Be sure to set the value of com.snc.pa.dc.max\_breakdown\_elements\_limit or com.snc.pa.dc.hsql.max\_breakdown\_elements\_limit property to be greater than or equal to sn\_ci\_analytics.max.search.threshold. The default value of these properties is 10000.

See [Breakdown and indicator Performance Analytics properties](https://www.servicenow.com/docs/access?context=pa-limit-setting-props&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) and [Data collector Performance Analytics properties](https://www.servicenow.com/docs/access?context=pa-dc-props&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Max event breakdown

</td><td>

sn\_ci\_analytics.max.event\_props.threshold

</td><td>

Sets the maximum breakdown elements for custom events. Default value is 100. Maximum can be 10000. Use this property in conjunction with the following properties in Performance Analytics. **Note:**

If the data on User Search Metrics page does not load due to an invalid configuration error, set the value of com.snc.pa.scorecards.max\_breakdown\_elements property to 10000. The default value of this property is 1000.

If the number of custom events exceeds the limit specified in the com.snc.pa.dc.max\_breakdown\_elements\_limit property, the dashboard will not show any data. Be sure to set the value of com.snc.pa.dc.max\_breakdown\_elements\_limit or com.snc.pa.dc.hsql.max\_breakdown\_elements\_limit property to be greater than or equal to sn\_ci\_analytics.max.search.threshold. The default value of these properties is 10000.

See [Breakdown and indicator Performance Analytics properties](https://www.servicenow.com/docs/access?context=pa-limit-setting-props&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) and [Data collector Performance Analytics properties](https://www.servicenow.com/docs/access?context=pa-dc-props&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Conversational Analytics dashboard reference](conversational-analytics-dashboard-reference-pae.md)

