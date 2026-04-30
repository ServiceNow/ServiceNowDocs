---
title: Localization Framework Hub and Spoke architecture
description: Enable one central instance to fulfill translation requests submitted from other instances using the Localization Framework Hub and Spoke architecture. Install optional Localization Framework plugins to configure one of your instances as a hub and other instances as spokes.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Framework Hub and Spoke architecture

Enable one central instance to fulfill translation requests submitted from other instances using the Localization Framework Hub and Spoke architecture. Install optional Localization Framework plugins to configure one of your instances as a hub and other instances as spokes.

By default, translations are requested and fulfilled on the same instance. However, in the Xanadu release, there is an available hub-spoke model for translation requests and fulfillment. With this architecture, translation requests are a two-step process:

1.  The spoke instance submits a translation request to the hub instance.
2.  The hub instance manages the fulfillment of the request, such as by sending the content to a translation management system \(TMS\). The hub returns the translated contents to the spoke instance.

Consider the Localization Framework Hub and Spoke architecture when you want to limit fulfillers' access to one instance only.

To set up this architecture, use the admin role to install the following plugins:

-   Localization Framework Hub \[com.sn.localization\_framework.hub\]. Install this plugin on the instance you designate as a hub.
-   Localization Framework Spoke \[com.sn.localization\_framework.spoke\]. Install this plugin on the instances you designate as spokes.

For more information on installation, see [Activate Localization Framework](../task/activate-lf-plugin.md).

When both plugins are installed, use the admin or localization\_admin role to configure the connection between hub and spoke instances. On the hub instance:

1.  Navigate to **Localization Framework** &gt; **Hub** &gt; **Spoke Settings.**
2.  In the **Name** field, enter a unique name for each entry.
3.  In the tab for **Translation Preferences**, find the **Translation Management System** \(TMS\) section. Enter the TMS service your organization uses.
4.  In the tab **Workflow Preferences**, configure according to your requirements. Depending on the workflow you choose, different subfields are populated.
5.  The tab **Project Preferences** is optional. If no project is entered, any request for translations into more than one target language is broken into separate tasks, one for each language.

**Note:** If Dynamic Translation is not installed, the option for machine translation is not available.

On a spoke instance:

1.  Navigate to the **Settings All Artifacts** table \[sn\_lf\_setting\].
2.  In the tab **Translation Preferences**, find the **Translation Management System** \(TMS\) section.
    -   **Enable TMS**: select.
    -   **TMS**: Set to `Localization Framework Hub`.
    -   **TMS Additional Info**: for **spokeSettingsName**, enter the name of the connection setting that has been configured on the hub.
3.  Navigate to the **Connection &amp; Credential Aliases** table. Find and open the record named **Localization Framework Hub TMS**.
4.  Add the connection to the hub in the **Connections** tab. You can enter the URL to your hub in the **Connection URL** field. Set authentication and other attributes appropriate to your environment.

From the perspective of the spoke instance, the hub acts as a TMS.

**Parent Topic:**[Configure the Localization Framework](configuring-localization-framework.md)

