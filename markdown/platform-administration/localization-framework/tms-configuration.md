---
title: Translation Management System configurations
description: The Localization Framework supports integration with a translation management system to localize the content.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translation Management System configurations

The Localization Framework supports integration with a translation management system to localize the content.

The TMS configuration table lists all the TMS services configured in the instance.

RWS and XTM TMS services are automatically enabled in Localization Framework with the activation of the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) and appear in the TMS configuration \[sn\_lf\_tms\_config\] table.

To use the RWS TMS service for localization of the artifacts, you must configure the connection and credentials. For more information about configuring RWS TMS, see [RWS Translation Management System spoke](sdl-spoke.md).

To use the XTM TMS service for localization of the artifacts, you must configure the connection and credentials. For more information about configuring XTM TMS, see [XTM Translation Management System spoke](xtm-spoke.md).

You can also sign up and create an account with a TMS service of your choice. To create and configure a custom TMS, see [Create a custom translation management system](../task/create-custom-tms.md).

-   **[RWS Translation Management System spoke](sdl-spoke.md)**  
The RWS Translation Management System spoke provides subflows and actions to localize the artifacts using the RWS translation management system service.
-   **[Configure RWS TMS in the Localization Framework](../task/configure-sdl-tms.md)**  
Configure RWS TMS to use the RWS TMS service in the Localization Framework.
-   **[XTM Translation Management System spoke](xtm-spoke.md)**  
The XTM Translation Management System spoke provides subflows and actions to localize the artifacts using the XTM translation management system service.
-   **[Configure XTM TMS in the Localization Framework](../task/configure-xtm-tms.md)**  
Configure XTM TMS to use the XTM TMS service in the Localization Framework.
-   **[Integrate with a translation management system](../task/integrate-with-tms.md)**  
Integrate with any translation management system of your choice to localize the artifacts requested for translations.
-   **[Create a custom translation management system](../task/create-custom-tms.md)**  
Configure Localization Framework with a third-party translation management system of your choice to localize an artifact.

**Parent Topic:**[Localization Framework settings](localization-settings.md)

