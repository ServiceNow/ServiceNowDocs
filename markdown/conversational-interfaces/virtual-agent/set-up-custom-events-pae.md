---
title: Create custom events to monitor
description: Create custom events and monitor them in the Conversational Analytics dashboard.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up the Conversational Analytics dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Create custom events to monitor

Create custom events and monitor them in the Conversational Analytics dashboard.

## Before you begin

Role required: Chat Analytics Admin.

## About this task

An event is a combination of conditions that apply to a subset of Virtual Agent \(VA\) conversations. For example, an event might be conversations originating on a Slack channel that VA transferred to a live agent.

Most metrics you see on the dashboard, for example topic and conversation details, are derived from pre-built events. The dashboard displays these events on the **Topics** and **Conversations** tabs. To build custom events, you can use the Custom Events feature. Use custom events to create analytics about data you're interested in, for example:

-   Number of conversations on a Slack channel that transferred to a live agent.
-   Number of conversations on a Slack channel where the user never returned.

![Virtual Agent Custom Events tab.](../images/dashboard-custom-events-dashboard-2-pae.png)

Custom events appear on the **Custom Events** tab. If you haven't configured any custom events, the dashboard won't display any. You can create up to 20 custom events.

Custom events take effect when you create them. You cannot use them to analyze data collected before you created the custom event.

## Procedure

1.  Navigate to **All** &gt; **Conversational Analytics** &gt; **Event Configuration** and select **New**.

    The Event New record page appears.

    ![Event new record form.](../images/dashboard-event-config-new1.png)

2.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Custom event's name.|
    |**Type**|Choose **Custom**. Choosing any other type changes the default behavior of the dashboard and is not recommended. This field specifies the type of event to include in the dashboard analytics.|
    |**Source table**|Table of conversations to examine to detect custom events.|
    |**Source Table Filter**|Use the condition builder to select specific data from the source table.|
    |**Conversation Mapping Field**|Maps fields in the source table to fields in another conversation-related table. For example, a channel metadata column in the interaction table can be mapped to the sys ID column of the conversation table. Every event must be mapped to a Conversation ID.|
    |**Active**|Select the check box to enable the custom event.|
    |**Event Time**|Specifies a time-based event, such as the time VA transferred a chat to a live agent. Selecting this check box opens the **Event Time Field**.|
    |**Event Time Field**|Specifies the time in an event that you want to monitor, for example, the time a chat was transferred to a live agent. This field appears when you select **Event Time**.|
    |**Apply Post Fetch Filter**|Enables you to use a script to filter data that was already filtered by the condition builder, **Source Table Filter**.|
    |**Post Fetch Script**|Text field to enter a script that filters the data that has been filtered by the **Source Table Filter**. This field appears when you select **Apply Post Fetch Filter**.|

3.  Click **Submit**.

    The Events page appears, which lists all custom events. You've specified the table to look for custom events. Now, you must specify the parameter values that trigger the custom event.

4.  Click the custom event you created.

5.  In the Event Properties related list, select **New**.

    The Event Property New Record page appears where you specify the properties for a custom event that you want to track on the dashboard.

    ![Event Property new record form with Value Field selected.](../images/dashboard-event-property-new-record.png)

    In this example, the **Custom Event** tab shows metrics for **Updated by** for the custom event, Messages-from-Slack.

6.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Record name for the property you want to collect metrics on.|
    |**Event**|Name of the custom event associated with this property.|
    |**Advanced**|Selecting this check box opens a text field in which you can enter a script that specifies the field value you want to filter on. Selecting this check box removes the **Value Field** field.|
    |**Value Field**|Specifies the field you want to collect metrics on.|
    |**Application**|The scope of the custom event.|
    |**Event Source Table**|The same value for this field you entered on the Event New Record page.|

7.  Click **Submit**.

    The Event page appears.

8.  Click **Update**.

    The Events page appears, which lists all custom events. You can open the **Custom Events** tab on the dashboard to see the custom event. This custom event is not retroactive; the dashboard only displays new events that satisfy the custom event criteria.


**Parent Topic:**[Setting up the Conversational Analytics dashboard](../concept/setting-up-va-dashboard-overview1-pae.md)

