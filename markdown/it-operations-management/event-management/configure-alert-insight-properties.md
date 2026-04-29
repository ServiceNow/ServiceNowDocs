---
title: Alert insight properties
description: Use these properties to configure alert insight.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert insight properties

Use these properties to configure alert insight.

The role required: evt\_mgmt\_admin

The following alert\_insight properties are under sys\_properties.

<table id="table_zm2_n3c_y2b"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Time Frame

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_alert\_history\_min

</td><td>

Set the time frame \(in minutes\) to retrieve repeated and similar alert data. Default `43200` \(30 days\)**Note:** Alerts are retrieved regardless of their state \(open / reopen / flapping / closed\).

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_closed\_alert\_window

</td><td>

Set the time frame \(in minutes\) to retrieve alerts that were already closed. It is the time after the alert last updated date. Default: `4320` \(3 days\)

</td></tr><tr><td class="sub-head" colspan="2">

Similarity

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_alert\_same\_as\_filter

</td><td>

This property is a comma-separated string that defines which of the alert fields is used to consider alerts to be similar. Default: `source,type,resource,metric_name`

</td></tr><tr><td class="sub-head" colspan="2">

Related CIs

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_related\_cis\_topology\_levelsThe relationship types are:

-   CMDB based \(metadata rules and suggested relations\)
-   Within application services
-   Within Alert groups

</td><td>

For ‘Within application service’ relationship type, this property sets the depth or the maximum level of relationship of retrieved CIs. Default: `3`

</td></tr><tr><td class="sub-head" colspan="2">

Score

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_group\_mapping

</td><td>

This property sets the score for within alert group relations. Default: `2`

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_level\_1\_mapping

</td><td>

This property sets the score for level 1 relationship. Default: `3`

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_level\_2\_mapping

</td><td>

This property sets the score for level 2 relationship. Default: `2`

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_level\_3\_mapping

</td><td>

This property sets the score for level 3 relationship. Default: `1`

</td></tr><tr><td class="sub-head" colspan="2">

Maximum related tasks

</td></tr><tr><td>

evt\_mgmt.alert\_insight\_max\_tasks

</td><td>

Maximum related tasks to retrieve for alert insight. Default: `10`

</td></tr></tbody>
</table>## Metadata rules consideration

The parent-child relationship of CIs is considered. Dependent relationship rules consist of hosting and containment rules, each type modeling the data from a different perspective of the CI.

To manage dependent relationship rules:

-   To access rules at the class level, use the CI Class Manager. Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.
-   To access grouped rules, use the Metadata Editor. Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Metadata Editor**.

Containment rules represent configuration hierarchy of CIs, describing which CI contains which other CIs.

Hosting rules represent placement of CIs in a business definition, describing what CIs run on.

Modify the alert insight properties to configure the way alert information and analysis appears in the Alert Insight pane.

## Related CIs configuration

The following properties control which CMDB relationships to consider for related CIs. The CMDB relationships include regular CMDB relation rules, metadata rules \(containment rules and hosting rules\), and suggested relations.

|Property|Usage|
|--------|-----|
|evt\_mgmt.related\_cis\_get\_all\_relation\_types|Get all relation types, not including metadata rules. Default: `false`|
|evt\_mgmt.related\_cis\_use\_containment\_rules|Use metadata containment rules. Default: `true`|
|evt\_mgmt.related\_cis\_use\_hosting\_rules|Use metadata hosting rules. Default: `true`|
|evt\_mgmt.related\_cis\_use\_suggested\_relations\_rules|Use suggested relations rules. Default: `false`|
|evt\_mgmt.related\_cis\_validate\_relation\_rules|This property controls whether to validate relation of CI according to metadata rules. Default: `true`|

## Score

Scores are configured per relation type or depth. Scores are accumulated. The higher the score, the more relevant is the related CI to the current CI.

**Example:**For a CI that was found at level `2` in the same application service of the current CI, the score is `2`. The same CI is in the same alert group, so there is an extra score of `3`. The accumulated score is therefore `2+3 = 5`.

## Affiliation type

The Affiliation Type column in the **Related Incidents**, **Related Change Requests**, and **Related Problems** tabs shows the type of relationship that the CI of the selected alert and the related CI have.

To see affiliation type relationships, navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Metadata Editor**.

The parent-child relationship between configuration items is considered.

**Parent Topic:**[Manage and monitor alerts](../concept/c_EMAlert.md)

