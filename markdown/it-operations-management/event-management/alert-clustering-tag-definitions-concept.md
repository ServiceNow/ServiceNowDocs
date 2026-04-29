---
title: Tag cluster alert grouping
description: Tag cluster alert grouping enables you to easily create groups of alerts. It is a non-code method of alert grouping that correlates alerts without having to use CMDB or model training. This simpler way of grouping similar alerts reduces the overall noise of a large quantity of alerts.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Mixed alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Tag cluster alert grouping

Tag cluster alert grouping enables you to easily create groups of alerts. It is a non-code method of alert grouping that correlates alerts without having to use CMDB or model training. This simpler way of grouping similar alerts reduces the overall noise of a large quantity of alerts.

Tag cluster alert grouping is enabled immediately after the activation of the Tag-Based Alert Clustering Engine application, available in the ServiceNow Store. This grouping is applied according to the correlation logic order specified in the [Configure alert correlation logic order](../task/configure-alert-correlation-logic-order.md). Alert grouping tags are attached to definitions on a many-to-many \(M2M\) basis. Multiple tags can be linked to a single definition, and a tag can be part of multiple definitions. Groups formed from tag cluster alert grouping definitions are classified as the Tag Cluster group type.

Tag cluster alert grouping supports domain separation, allowing different domains to have their own distinct alert grouping configurations and logic.

First, create alert grouping tags to define the criteria for grouping alerts. You can set the tags to require an exact match, an approximate \('fuzzy'\) match, or a character pattern match.

You can also use preconfigured tags to speed up alert clustering. These predefined tags are mapped from alerts and are based on information from sources such as the Alert field, Alert tags, or Alert additional info. If the required data is missing and the selected tag source is Alert CI or Alert CI key, the tag is populated using the Configuration Item \(CI\) value from the Configuration Management Database \(CMDB\). Predefined tags are easily identified by their description, which includes out of the box.

You can attach one or more tags to an alert clustering definition, which specifies the conditions for alert correlation. You can either create your own alert clustering definition or use a predefined one provided by the application. Predefined definitions come with associated tags.

**Important:** Make sure to activate predefined definitions before use. In new systems, several definitions are active by default. The remaining ones must be activated. For more information, see [Activate a predefined alert clustering definition](../task/alert-clustering-predefined-definition.md).

Once one or more alert clustering tags are attached to a definition, the system collects alerts and checks if their tags match all the tag values specified in the definition. Alerts with matching or similar tag values are grouped together. New incoming alerts join an existing group if their tags match the tags in the definition used to create the group.

For tag-cluster grouping, alerts are added to a group based on the timeframe defined in the alert clustering settings. The time between the initial alert \(virtual alert\) and subsequent alerts is evaluated. If two new alerts are received, and their time difference falls within the defined timeframe, they are added to the group. The initial event's generation time is used to determine the relevance of the timeframe.

**Related topics**  


[Create alert clustering tags](../task/alert-clustering-tags.md)

[Create an alert clustering definition](../task/alert-clustering-definitions.md)

[Activate a predefined alert clustering definition](../task/alert-clustering-predefined-definition.md)

[Attach a predefined tag to a tag-based alert grouping definition](../task/alert-clustering-predefined-tag.md)

[Configure an event rule to customize alert content](../task/t_EMComposeOuput.md)

[Alert tags](alert-tags.md)

