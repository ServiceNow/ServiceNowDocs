---
title: Enable application installation tracking through an update set
description: You can add specific applications or versions as an app installation and configure to track them in an update set.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, System update sets, Deploying applications, Building applications]
---

# Enable application installation tracking through an update set

You can add specific applications or versions as an app installation and configure to track them in an update set.

## Before you begin

Role required: admin

This is applicable only to **Global** update sets.

Automatic tracking is on by default. You can turn off automatic tracking by locating the `glide.update_set.track_installs_enabled` system property and setting it to `false`.

## Procedure

1.  To manually configure app installation track through an update set do the following.

2.  Navigate to **All** &gt; **sys\_store.LIST**.

3.  Select the update set to configure in the store apps list.

4.  Select **Add app install to current update set** in the related links section.

    A message appears notifying you to confirm tracking app installs in the update set.

5.  You can also configure app installs by navigating to **All** &gt; **v\_plugin.LIST**

6.  Select the plugin to configure from the system plugin list.

7.  Select **Add app install to current update set** in the related links section.

8.  Select **Update**.

    A message appears notifying you to the confirm app installs for the update set.


