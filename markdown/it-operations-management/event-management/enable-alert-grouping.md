---
title: Configure scheduled job-based alert grouping
description: Set up rules and parameters to group related alerts automatically, streamlining alert management and reducing alert noise.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Scheduled jobs and parameters for alert grouping, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure scheduled job-based alert grouping

Set up rules and parameters to group related alerts automatically, streamlining alert management and reducing alert noise.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The scheduled job Service Analytics: Group Alerts Using RCA/Alert Aggregation helps in grouping alerts.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Alert Correlation Properties**.

2.  On the Alert Correlation Properties page, enable the relevant properties.

    -   Enable alert aggregation for Automated, CMDB, and Text-based groups \(**sa\_analytics.aggregation\_enabled**\).

        **Note:** When disabled, disables all other groups.

    -   Enable alert aggregation for CI-based Automated groups \(**sa\_analytics.specific\_patterns\_enabled**\).
    -   Enable CMDB correlation for alert aggregation \(CMDB groups\) \(**sa\_analytics.agg.query\_cmdb\_correlation\_enabled**\).
    -   Enable alert aggregation for Text-based groups \(**sa\_analytics.text\_based\_group\_enabled**\).
    -   “Group by” property, with comma-separated list of field names that need to have matching values across alerts to allow alerts to be grouped together. The property can contain alert field names \(such as assignment\_group\), CI field names \(such as alert\_cmdb\_ci.location\), alert additional info field names \(such as additional\_info.state\) or alert tags \(such as t\_data\_center\). When the specified field values match each other between alerts, those alerts can be grouped together \(**sa\_analytics.agg.group\_alert\_with\_same\_group\_by\_fields**\).
    -   Max number of relations between CIs in a topology which form a CMDB group \(**sa\_analytics.agg.query\_cmdb\_graph\_walk\_nodes**\).
    -   Use all CMDB relations for CMDB group correlation. This property impacts both CMDB group correlation and Alert Similarity on the Alert form \(**evt\_mgmt.related\_cis\_get\_all\_relation\_types**\).
3.  Select **Save**.

    To group alerts without a CI as Text-based or CI-based groups, set **sa\_analytics.enable\_no\_ci\_grouping** to `true`. Ensure the Feature Identifier includes both the node and metric name. For details on configuring the feature identifier, see [Specify and manage pattern identifier attributes for alert aggregation](ptrn-attributes-alrt-aggregate.md).

4.  Set **evt\_mgmt.alert\_groups\_reasoning.enable\_worknotes** to `none` to prevent group reasoning work note display.

    By default, a work note appears in the **Activities** tab when a group is created or updated, showing the grouping reason.


**Related topics**  


[Automated alert grouping](../concept/c_SACorrelatedAlertGroups.md)

[CMDB based alert grouping](../concept/cmdb-alert-groups.md)

[Text-based alert grouping](../concept/text-based-alert-groups.md)

[Tag cluster alert grouping](../concept/alert-clustering-tag-definitions-concept.md)

