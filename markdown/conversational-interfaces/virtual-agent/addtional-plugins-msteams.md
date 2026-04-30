---
title: Plugins for Conversational Integration with Microsoft Teams
description: Activate the Glide Virtual Agent \[com.glide.cs.chatbot\] plugin, the Conversational Integration with Microsoft Teams \[sn\_va\_teams\] plugin, and verify its additional plugins to enable other features for conversation design.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-08-06"
reading_time_minutes: 1
breadcrumb: [Integrating Virtual Agent with Microsoft Teams using the self-configured bot, Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Plugins for Conversational Integration with Microsoft Teams

Activate the Glide Virtual Agent \[com.glide.cs.chatbot\] plugin, the Conversational Integration with Microsoft Teams \[sn\_va\_teams\] plugin, and verify its additional plugins to enable other features for conversation design.

You must have either the virtual\_agent\_admin or admin role and the external\_app\_install\_admin role to activate these additional plugins. For details, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Note:** Ensure that you have performed the following steps before verifying the activation of additional plugins required for Microsoft Teams.

-   Installing of the Glide Virtual Agent \[com.glide.cs.chatbot\] plugin.

    For more information about activating the Glide Virtual Agent plugin, see [Activate Virtual Agent](../task/activate-virtual-agent.md).

-   Downloading the Conversational Integration with Microsoft Teams app from the ServiceNow® Store.

    For more information about downloading the app, Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   Installing the Conversational Integration with Microsoft Teams \[sn\_va\_teams\] plugin in your ServiceNow instance.

    For more information about installing Conversational Integration with Microsoft Teams, see [Install Conversational Integration with Microsoft Teams](../task/teams-install.md).


Verify the following plugins for Conversational Integration with Microsoft Teams.

-   Microsoft Teams Graph Spoke \[sn\_msteams\_ahv2\]: Plugin is auto installed as part of \[sn\_va\_teams\]. In your ServiceNow instance, navigate to **All** &gt; **sys\_plugins.list** and search for \[sn\_msteams\_ahv2\] to locate the plugin. If it has not been installed, you might have to request from the ServiceNow Store first and install the plugin in your ServiceNow instance.
-   MS Teams - App Core \[com.snc.msteams.app.core\]: Plugin is auto installed as part of \[sn\_va\_teams\]. In your ServiceNow instance, navigate to **All** &gt; **sys\_plugins.list** and search for \[com.snc.msteams.app.core\] to locate the plugin. If the plugin is installed, you are all set to move forward. If it was not installed, reach out to Customer Service and Support.

