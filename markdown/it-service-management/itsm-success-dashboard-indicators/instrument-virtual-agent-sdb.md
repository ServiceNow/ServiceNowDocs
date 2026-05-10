---
title: Configure Virtual Agent topics for ITSM Success Dashboard indicators
description: Configure the Virtual Agent \(VA\) topics for ITSM Success Dashboard indicators so that data is displayed correctly if you have topics other than the base system topics.
locale: en-US
release: australia
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Virtual Agent topics for ITSM Success Dashboard, ITSM Success Dashboard Admin console, Configure, ITSM Success Dashboard indicators, IT Service Management]
---

# Configure Virtual Agent topics for ITSM Success Dashboard indicators

Configure the Virtual Agent \(VA\) topics for ITSM Success Dashboard indicators so that data is displayed correctly if you have topics other than the base system topics.

## Before you begin

Role required: admin

## About this task

Map the topics with deflection patterns of the **ITSM VA Default** deflection tracker. Deflection trackers helps in analysing the performance of a conversation and how helpful Virtual Agent topics are for users.

Modify the URL for the **Link Output** in a topic to set the referrer to va so that when a catalog item is submitted, the item is calculated as a submission from Virtual Agent.

## Procedure

1.  Navigate to **All &gt; Virtual Agent &gt; Designer**.

2.  Select the topic for which you want to add the deflection tracker.

3.  Enable the flow chart view by disabling the **Table View** toggle switch.

4.  Drag and drop the **Deflection** node from the **Utilities** section to the place in the flowchart where you want to add the deflection pattern.

5.  Enter the following details in the Deflection Properties pane on the right.

<table id="table_tbt_4rj_25b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Deflection Configuration

</td><td>

ITSM VA Default

</td></tr><tr><td>

Deflection Pattern

</td><td>

-   **ITSM VA-Self-Resolving:** When the node in the topic indicates that Virtual Agent is able to resolve the user problem completely without creating an IT ticket \(incident or request\) and consequently contributing to the Self-solved KPIs.
-   **ITSM VA-Triage &amp; Created:** When the node in the topic indicates that an IT ticket \(incident or request\) was submitted using Virtual Agent and consequently contributing to the call deflection KPIs.


</td></tr><tr><td>

Activity Table

</td><td>

Table where the deflection activity occurs. This table is associated with the primary activity table. For more information, see [Create deflection configurations and patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/set-up-deflection-settings-va.md).

</td></tr><tr><td>

Activity Ids

</td><td>

List of comma-separated activity system IDs.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  Select **Link Output** in the flow chart.

8.  Select the url in the **Link** field in the Link response pane on the right.

9.  Append the URL with `&referrer=va`.

10. Select **Save**.


**Parent Topic:**[Configure Virtual Agent topics for ITSM Success Dashboard](../concept/configure-va.md)

**Related topics**  


[Tracking deflections using deflection topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/deflections-virtual-agent.md)

[Create deflection configurations and patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/set-up-deflection-settings-va.md)

