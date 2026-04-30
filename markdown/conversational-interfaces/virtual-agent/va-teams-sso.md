---
title: Configuring smart links in Microsoft Teams
description: Configure smart links for your Virtual Agent app in Microsoft Teams to enable different link opening experiences.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Configuring, smart links, Microsoft Teams, MSTeams, Virtual Agent, Task module]
breadcrumb: [Configure link authentication and opening experience in Microsoft Teams, Configure Virtual Agent for Microsoft Teams, Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configuring smart links in Microsoft Teams

Configure smart links for your Virtual Agent app in Microsoft Teams to enable different link opening experiences.

Smart link settings in the admin console enable admins to define one of the three link opening options in Microsoft Teams.

1.  Microsoft Teams task module/pop-up
2.  Microsoft Teams tab
3.  New browser tab

Through link authentication and Single Sign-On \(SSO\) support, link content can be rendered in a pop-up, Microsoft Teams tab, or a new browser tab.

You can configure smart links for Microsoft Teams from the URL navigation system action under **Target Location**. For more information about configuring smart links, see [Create a smart link preference](../../conversational-interfaces/task/create-smart-link-preference.md).

There are three valid link opening options that are applicable to Microsoft Teams and the smart link settings in admin console enables admins to define where to open a link in Microsoft Teams.![Valid link opening options applicable to Microsoft Teams. Load in Place, New Browser Tab, and Popup options are highlighted.](../images/msteams-link-open-options.png)

1.  **Load in Place**: Links open inside a Microsoft Teams tab.

    **Note:**

    -   Only ServiceNow links are supported currently.
    -   While **Load in Place** is always an option for admins to choose from, this functionality is only supported when admins have already installed an additional tab within Microsoft Teams \(for example, Employee Center tab as part of the ITSM/HR plugins\).
    -   Admins must ensure that the following steps are complete:
        -   MS Teams - App Core \(com.snc.msteams.app.core\) plugin is installed as part of ITSM/HR plugins and additional tab has already been enabled.
        -   The **sn\_va\_teams.view\_msft\_tab** system property is set to true.
        -   The link authentication status on your ServiceNow instance is green.
2.  **New Browser Tab**: Links open in a new browser tab \(a new tab in Google Chrome, Safari, etc.\).
3.  **Popup**: Links open in a pop-up/task module in Microsoft Teams. When pop-up is selected, admins also have the option of selecting a pop-up size of Small, Medium, or Large. The default size is Large.​

    Before you start configuring pop-up using Target location, double check that the value of **sn\_va\_teams.view\_non\_video\_msft\_task\_module** system property is **true**. When the link authentication status is active from the previous step, the value is automatically set to **true**. When this system property is true, you can use the pop-up. If you want to disable pop-up in Microsoft Teams, you can manually set this property to **false**.

    **Note:** Only ServiceNow links are supported currently.


When no conditions are specified on the Target Location record, the valid link opening mechanism applies to both chat widget and Microsoft Teams in a way that makes sense to its host application. For example, if admins specify a URL pattern to be opened using **Load in Place** without any conditions, the link on chat widget opens by refreshing the topmost browser frame \(chat widget's unique behavior\). However, the same link opens in a Microsoft Teams tab.

If both chat widget and Microsoft Teams are valid channels for the customer, then admins can define different target locations for each channel by specifying the device type in the condition field \(such as Teams and mweb\). If the device type is specified as Teams and no other device types are specified, then that particular target location record will only be applied in Microsoft Teams.

**Parent Topic:**[Configure link authentication and opening experience in Microsoft Teams](../task/link-opening-authentication-msteams.md)

