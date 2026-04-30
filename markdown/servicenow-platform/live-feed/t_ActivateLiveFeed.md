---
title: Activating Live Feed
description: Live Feed is active for all instances. An administrator can activate the Live Feed plugin if it is not already active.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activating Live Feed

Live Feed is active for all instances. An administrator can activate the Live Feed plugin if it is not already active.

## Before you begin

Role required: admin

**Important:**

Core UI is required to use Live Feed. Live Feed is not supported in Next Experience. If you turn on Next Experience, Live Feed is automatically disabled and will no longer work. See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

While Live Feed has been discontinued, we are always exploring new ways to enhance our services. Stay tuned for future updates and improvements.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


