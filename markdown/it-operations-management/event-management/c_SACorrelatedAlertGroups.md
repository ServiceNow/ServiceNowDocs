---
title: Automated alert grouping
description: Event Management alert aggregation aggregates alerts into automated alert groups based on historical alert data. Automated alert groups are displayed in the Express List in the Service Operations Workspace.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Automated alert grouping

Event Management alert aggregation aggregates alerts into automated alert groups based on historical alert data. Automated alert groups are displayed in the Express List in the Service Operations Workspace.

Enable creating automated alert groups by setting the **Enable alert aggregation for Automated, CMDB and Text based groups** \(**sa\_analytics.aggregation\_enabled**\) property to **true**.

If the Domain Support - Domain Extensions Installer is activated, then alert aggregation patterns are built according to the domain level that is specified in the **sa\_analytics.agg.learner\_domain\_level** property. By default, the domain level is set to two, which is the second domain level in the domain hierarchy. See [Domain separation and Event Management](domain-separation-event-management.md).

To create automated alert groups, aggregation algorithms rely on historical alerts with the same alert identifier \(CI and metric identifier\) and which occurred multiple times in the same time frame.

## About Pattern Identifiers

The default pattern identifier is defined as Metric Name. In the Manage Pattern Identifier form you can which alert fields are currently used for the pattern identifier. You can choose a different set of alert fields to deploy, or define a new set of fields for the pattern identifier.

**Note:** A set of alert fields used for pattern identifier is also referred as **Feature Identifier Attributes** or attributes.

To ensure that the specified alert fields in the pattern identifier are effective, a sufficient number of alerts must have the respective populated fields. Therefore, if you specify a new set of alert fields in the pattern identifier, do the following to ensure meaningful analysis:

-   Create an event rule that populates the respective alert fields.
-   If a large number of existing alerts don’t have values for the new set of alert fields used in the pattern identifier, ensure to run the **Service Analytics Attribute Populator for Historical Alerts** job that uses the appropriate event rule to populate alert fields from historical alerts. Properties originating from the CMDB CI using dot-walking aren’t populated.
-   Choose effective identifiers:
    -   Ensure that the set of alert fields in the pattern identifier isn’t too unique \(for example, the date field is unique for every alert\), because it is impossible to identify any pattern.
    -   Ensure that the set of alert fields in the pattern identifier isn’t too common, because it won’t be possible to create distinct groups, as everything would be included in the same group.

When an alert pattern is discovered based on a set of alert fields, the alerts are considered to be related to each other and therefore are grouped into a Learned Pattern. For example, if you configure identifier attributes to create a pattern based on alerts with the same **Priority Group** and **Resource**, if a group of alerts match those attributes, they’re grouped into a pattern that displays on the **Learned Patterns** report \(**Event Management** &gt; **Administration** &gt; **Learned Patterns**\).

Only one set of pattern identifier attributes can be active at a time. A new set of pattern identifier attributes isn’t automatically implemented until you deploy it. When you deploy a new set of attributes, the current set of attributes that is in effect becomes inactive. Subsequent queries use the active pattern identifier attributes to perform alert aggregation.

The major purpose of this pattern based alert aggregation is to find patterns of issues that occurred during last 30 days. The number of days is controlled by the **sa\_analytics.agg.learner\_period\_days** parameter. To identify an issue, the system uses a combination of Configuration Items \(CIs\) and Pattern Identifiers \(sometime called Feature Identifiers\). A Pattern Identifier, by default, is defined as Metric Name, but it may be modified. Two alerts are similar if they have the same CI and Pattern Identifier. However, Source, Severity, Description, and other alert fields may differ. For more information, see [Specify and manage pattern identifier attributes for alert aggregation](../task/ptrn-attributes-alrt-aggregate.md).

**Note:** The Alert Aggregation Learner also learns the patterns of alerts in manual alert groups.

In some cases you can build patterns from alerts whose CIs have the same value in a selected field. For example, to build patterns from alerts that have the same CI Location field, enter 'location' in the **sa\_analytics.agg.learner\_group\_by\_property** property. For more information, see [Configure scheduled job-based alert grouping](../task/enable-alert-grouping.md).

Alerts that don't contain a CI can still be grouped together as Text-based or CI-based alert groups. In this case, a node is considered as a CI. To enable this functionality, set the **sa\_analytics.enable\_no\_ci\_grouping** property to true. When working with CI-based groups, ensure that the Feature Identifier includes both the node and metric name. For details on configuring the feature identifier, see [Learned Patterns report](c_SALearnedPattersReport.md).

**Related topics**  


[CMDB based alert grouping](cmdb-alert-groups.md)

