---
title: Enable system properties for Knowledge Center
description: To use the Knowledge Center plugin, you must enable the system properties before you configure the space.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable system properties for Knowledge Center

To use the Knowledge Center plugin, you must enable the system properties before you configure the space.

## Before you begin

The default system properties settings for Knowledge Center:

-   **For new users:** All the properties are enabled \(set to **true**\) by default, encouraging immediate use of the new system.
-   **For existing users:** All the properties are disabled \(set to **false**\) by default to avoid disrupting current workflows or customizations. Existing users must manually enable the properties to access KC and its features.

**Supporting releases**: Knowledge Center and its features are available to the users in Yokohama Patch 11 \(YP11\) and Zurich Patch \(ZP4\) releases.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Center** &gt; **System Properties**.

    ![Knowledge Centre system properties.](../image/KC-AO-system-properties.jpeg)

2.  Enable the following system properties by setting the parameter to **true**.

    |System property|Description|
    |---------------|-----------|
    |**__sn\_km\_center.glide.knowman.enable__**|Provides access to the Knowledge Center and its features. It must be set to true to enable agents to access the plugin and use its features.|
    |**__sn\_km\_center.glide.knowman.ece.enable__**|Governs access to the Knowledge Center Article Editor. If set to true, you get access to the enhanced editor capabilities. If set to false, the legacy TinyMCE editor remains available. As there are compatibility gaps between Article Editor and TinyMCE, you can choose based on your training and workflow requirements. Disabling this property also restricts access to article optimization features.|
    |**__sn\_km\_center.glide.knowman.redirect.enable__**|Controls how links to the Knowledge Center behave. If set to true, you will experience all the KC features in the new interface. If set to false, you will be redirected to the Core UI interface, which may be necessary for those with customizations incompatible with the new system. It allows you to use the KC features, while retaining access to legacy forms for compatibility.|


