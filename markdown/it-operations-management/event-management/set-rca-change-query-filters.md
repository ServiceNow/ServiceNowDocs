---
title: Customize RCA settings
description: Modify default settings that determine RCA behavior.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Probable Root Cause Analysis \(RCA\), Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Customize RCA settings

Modify default settings that determine RCA behavior.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Default filter settings control which change requests RCA considers as possible root causes. You may want to change certain default settings, for example to make RCA ignore standard change requests.

You can also change the number of probable root causes shown in the list. By default, the list shows the five probable root causes with the highest root cause score.

By default the RCA calculation is enabled. You can disable it by changing the default **sa\_analytics.disable\_prc** value to True.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Do one or both of the following, as needed.

    -   Change default filter settings:
        1.  Select **New**.
        2.  In the **Name** field, specify the name of the property for which you want to change the default setting.

            The new property must have the same name as the related property in the table.

<table id="table_sy4_pfg_slb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Type

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

sa\_analytics.rca.filter\_category

</td><td>

The categories of change requests that RCA considers as possible root cause.

</td><td>

string

</td><td>

" "

</td></tr><tr><td>

sa\_analytics.rca.filter\_type

</td><td>

The types of change requests that RCA considers as possible root cause.

</td><td>

string

</td><td>

"standard,normal,emergency"

</td></tr><tr><td>

sa\_analytics.rca.filter\_state

</td><td>

The state of change requests that RCA considers as possible root cause.

</td><td>

string

</td><td>

"-1,0,3,7,8,157"-   Implement: -1
-   Review: 0
-   Closed: 3,7,8,157


</td></tr><tr><td>

sa\_analytics.rca.filter\_interval\_in\_hour

</td><td>

The time frame, in hours, during which change requests occurred that RCA considers as possible root cause.

</td><td>

int

</td><td>

168

</td></tr><tr><td>

sa\_analytics.rca\_use\_legacy\_query

</td><td>

Use legacy queries for RCA calculation.

</td><td>

Boolean

</td><td>

True

</td></tr><tr><td>

sa\_analytics.rca.get\_tasks\_for\_impacted\_cis

</td><td>

Includes change requests for impacted services in the RCA list.

</td><td>

Boolean

</td><td>

True

</td></tr><tr><td>

sa\_analytics.rca\_scoring\_by\_alert\_proximity

</td><td>

Enables sorting of RCAs by time proximity to the alert.

</td><td>

Boolean

</td><td>

True

</td></tr><tr><td>

sa\_analytics.rca\_cmdb\_relations\_levels

</td><td>

Number of hops to search related configuration items.

</td><td>

int

</td><td>

1

</td></tr><tr><td>

sa\_analytics.rca\_time\_filtering\_by\_planned\_time

</td><td>

Enables filtering of change requests by planned time.

</td><td>

Boolean

</td><td>

True

</td></tr><tr><td>

sa\_analytics.rca\_time\_filtering\_by\_actual\_start\_time

</td><td>

Enables filtering of change requests by implementation time.

</td><td>

Boolean

</td><td>

True

</td></tr><tr><td>

sa\_analytics.rca.upper\_filter\_interval\_in\_hours

</td><td>

Determines the time upper bound for change requests filtering.

</td><td>

int

</td><td>

1

</td></tr><tr><td>

sa\_analytics.rca.order\_by\_scoring\_for\_virtual\_alerts

</td><td>

When calculating RCAs for virtual alert – order the records by scoring of PRCs of the corresponding secondaries.

</td><td>

Boolean

</td><td>

True

</td></tr><tr><td>

sa\_analytics.rca\_same\_reasoning\_use\_newer

</td><td>

When 2 PRCs have the same reasoning, prioritize the one with the most recent change request during scoring calculations.

</td><td>

Boolean

</td><td>

True

</td></tr><tr><td>

sa\_analytics.rca.prefer\_cr\_on\_app\_service

</td><td>

In case there is the same change request on application service and on CI, prefer the one from application service.

</td><td>

Boolean

</td><td>

False

</td></tr></tbody>
</table>        3.  Enter a valid value for the property.

            **Note:** The value you set for the new property overrides the default value for the related property.

    -   Change the maximum number of probable root causes shown in the list:
        1.  Find the property **sa\_analytics.rca\_task\_table\_max\_records**.

            |Property name|Description|Type|Default value|
            |-------------|-----------|----|-------------|
            |**sa\_analytics.rca\_task\_table\_max\_records**|The maximum number of probable root causes shown in the Probable root causes list.|int|5|

        2.  Replace the default value with a new valid value.
    -   Disable RCA by creating the **sa\_analytics.disable\_prc** property.
        1.  Select **New**.
        2.  Fill in the form with the following values.

            |Property name|Description|Type|Value|
            |-------------|-----------|----|-----|
            |**sa\_analytics.disable\_prc**|Disabling the Probable root cause.|Boolean|True|

3.  Click **Submit**.


**Parent Topic:**[Probable Root Cause Analysis \(RCA\)](../concept/probable-rca.md)

