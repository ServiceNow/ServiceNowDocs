---
title: Enable system properties for Knowledge Center
description: To use the Knowledge Center plugin, you must enable the system properties before you configure the space.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/enable-system-properties-for-KC.html
release: zurich
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable system properties for Knowledge Center

To use the Knowledge Center plugin, you must enable the system properties before you configure the space.

## Before you begin

The default system properties settings for Knowledge Center:

-   **For new users:** All properties are enabled \(set to **true**\) by default.
-   **For existing users:** All properties are turned off \(set to **false**\) by default to avoid disrupting current workflows or customizations. Existing users must enable the properties to access KC and its features.

**Supporting releases**: Knowledge Center and its features are available to the users in Yokohama Patch 11 \(YP11\) and Zurich Patch \(ZP4\) releases.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Center** &gt; **System Properties**.

    \[Omitted image "KC-AO-system-properties.jpeg"\] Alt text: Knowledge Centre system properties.

2.  Enable the following system properties by setting the parameter to **true**.

    |System property|Description|
    |---------------|-----------|
    |**__sn\_km\_center.glide.knowman.enable__**|Provides access to the Knowledge Center and its features. It must be set to true to enable agents to access the plugin and use its features.|
    |**__sn\_km\_center.glide.knowman.ece.enable__**|Governs access to the Knowledge Center Article Editor. If set to true, you get access to the enhanced editor capabilities. If set to false, the legacy TinyMCE editor remains available. As there are compatibility gaps between Article Editor and TinyMCE, you can choose based on your training and workflow requirements. Disabling this property also restricts access to article optimization features.|
    |**__sn\_km\_center.glide.knowman.redirect.enable__**|Controls how links to the Knowledge Center behave. If set to true, all KC features are available in the updated interface. If set to false, users are redirected to the Core UI interface, which may be necessary for customizations incompatible with the updated interface. You can use KC features while retaining access to legacy forms for compatibility.|
    |**__sn\_km\_center.ao\_auto\_update.enabled__**|Enables the auto-update feature for article optimization scans. When active, eligible multiple H1 tag and title relevancy findings can be auto-fixed from the Article Optimization dashboard. Active by default.|
    |**sn\_km\_gen\_ai.auto\_merge.enabled**|Enables the auto-merge feature for potential duplicate articles. If this property is not enabled, users are taken to the existing potential duplicate experience.|
    |**sn\_km\_gen\_ai.auto\_merge.revert\_ttl\_days**|Sets the default revert period, in days. After this period, automatically merged content and automatically updated content are no longer eligible for revert.|
    |**__sn\_km\_gen\_ai.auto\_merge.confidence\_threshold__**|Sets the minimum confidence score, as a percentage, that a potential duplicate article group must meet to be eligible for automatic merge and publish. Groups with a confidence score less than this threshold are routed to manual review instead.|


