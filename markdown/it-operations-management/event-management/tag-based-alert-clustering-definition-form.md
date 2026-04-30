---
title: Event Management tag based alert grouping definition form
description: The form for creating or modifying a tag based alert clustering definition displays detailed information about the definition.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management tag based alert grouping definition form

The form for creating or modifying a tag based alert clustering definition displays detailed information about the definition.

<table id="table_rqx_ysz_jrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the alert clustering definition.Definition names must be unique.

</td></tr><tr><td>

Active

</td><td>

Select to activate the definition. This option is selected by default.

</td></tr><tr><td>

Order

</td><td>

The order by which definitions are tested for incoming alerts. Those with lower Order values are tested first. When an alert matches one of the definitions' filters, it continues searching for more definitions.

 Default value = 1000

</td></tr><tr><td>

Domain

</td><td>

The domain in which the current record was created. Read-only.

</td></tr><tr><td>

Assignment group

</td><td>

Assignment group that works on the alert.If no assignment group is defined in the alert rule, then this alert rule is considered as a global rule.

When the rules are running – first the global rules run and then the rules that belong to the assignment group of the alert.

</td></tr><tr><td>

Description

</td><td>

Enter an optional description of the alert clustering definition.

</td></tr><tr><td>

Filter

</td><td>

Set conditions that incoming alerts must meet to be measured by the alert clustering definition's tags. If the tags correspond to alerts that exist in the system and are within the **Clustering timeframe \(minutes\)** value, the incoming alerts join with the existing alerts to form an alert group.After configuring the filter, you can click the **Preview** button to view how many existing alerts match the filter's condition.

**Note:**

-   Matching alerts are not automatically included together in an alert group. Alerts are grouped only if they have corresponding alert clustering tags.
-   Filter parameters are case sensitive by default. To disable case sensitivity, set the **sa\_analytics.correlation\_case\_sensitive** parameter to **false**.
-   You can also configure alert fields to be excluded from the search, using the **sn\_em\_tbac.tag\_excluded\_alert\_fields** property. By default, the following are excluded by this property:
    -   type
    -   event\_class

</td></tr><tr><td>

Override group description

</td><td>

Default group descriptions begin with a “Group of alerts” prefix, followed by the description of the primary alert in the group. You may override this group description by selecting the **Override group description** check box. Then, in the **Custom description** field, type a description. This description is used as the description of the groups that are created by this alert clustering definition. **Note:** You cannot save the form if you left the Custom description field blank or with the default 'Group of alerts' text.

</td></tr><tr><td>

Clustering timeframe

</td><td>

The maximum time, in minutes, allowed between the first alert and subsequent alerts for them to be grouped together. For example, a value of 60 indicates that any alert generated within 60 minutes of the first alert in the group \(the oldest alert\) is included in the alert group. Any alert generated after this 60-minute window from the initial alert is not included in the group.Permitted values = 0-1440

</td></tr><tr><td>

Tag Based Alert Clustering Definitions Tags M2M

</td><td>

Select the alert clustering tags to be assigned to the alert clustering definition. Alerts that meet the criteria specified in the selected tags are included in the alert group. The available options are the tags created on the **Tag Based Alert Clustering Tags** page.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

