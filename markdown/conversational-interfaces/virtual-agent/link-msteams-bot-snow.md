---
title: Integrate your self-configured bot with Microsoft Teams for GCC-H or DoD
description: Link your registered Microsoft Teams bot with your ServiceNow instance to integrate it with the Virtual Agent. Use your ServiceNow Virtual Agent application to install and configure Conversational Integration with Microsoft Teams.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Integrate, self-configure bot, Microsoft Teams, MSTeams, Virtual Agent, Conversational Integration, G-CCH, DoD]
breadcrumb: [Integrate VA with MS Teams for GCC-H, Specialized VA integrations for Teams, Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate your self-configured bot with Microsoft Teams for GCC-H or DoD

Link your registered Microsoft Teams bot with your ServiceNow instance to integrate it with the Virtual Agent. Use your ServiceNow Virtual Agent application to install and configure Conversational Integration with Microsoft Teams.

## Before you begin

Role required: virtual\_agent\_admin or admin and Microsoft Azure admin.

## Procedure

1.  Fetch the Tenant ID, Client ID \(Application ID\), Client Secret, and Bot Name details for your bot created in Microsoft Teams.

    For more information, see [Retrieve bot details](create-msteams-bot-gcch.md#bot-details).

    **Note:** Use this information when setting up the self-configured bot in your ServiceNow instance.

2.  As a ServiceNow admin, set up the self-configured bot on the ServiceNow instance in the global scope.

    1.  Log in to your ServiceNow instance and navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

    2.  In **General Settings** under **Channels**, select **View All**.

        The Channels and integrations page opens.

    3.  Under the Available Channels section in the Microsoft Teams tile, select **Add Integrations**.

        **Note:** The **Add Integrations** drop-down is available only after installing the Conversational Integration with Microsoft Teams plugin \(sn\_va\_teams\) on your ServiceNow instance.

        ![Microsoft Teams Add Integrations options. The Integrate with Self-configured bot option is selected.](../images/add-msteams-self-integ.png)

    4.  From the **Add Integrations** drop-down, select **Integrate with your self-configured bot**.

    5.  In the Integrate Microsoft Teams with self-configured bot page, provide the **Name of the bot**, **Tenant ID**, **Client ID \(App ID\)**, and **Client Secret** that you made a note while creating the Microsoft Teams bot and select **Submit**.

        ![Integrate Microsoft Teams with self-configured bot window in Conversational integrations Channels and integrations settings.](../images/msteams-multi-integ.png "Integrate Microsoft Teams with self-configured bot")

        **Note:** If you own multiple ServiceNow instances and would like to integrate additional bots for additional instances, repeat the preceding steps to add and integrate with bots.

        If you would like to integrate your ServiceNow instance with another Microsoft Teams bot, select the Plus icon against the Self-configured bot or select the **Add integration** drop-down on the Manage Microsoft Teams channel page and select **Integrate with your self-configured bot**.

        ![image.add-self-config-integ-2]

        For more information, see [Manage the ServiceNow Virtual Agent integration with Microsoft Teams](configure-va-teams.md).

        User receives a message that the installation is successful.

3.  In your ServiceNow instance, navigate to **System OAuth** &gt; **Application Registry** and open the record that contains the **sample-msteams-oauth-consumer**.

4.  Right-select on the grey bar header titled **OAuth OIDC Entity** on the top of the page to select **Configure** &gt; **Form Layout**.![OAuth OIDC Entity record page with Form Layout selected from Configure option.](../images/gcc-h-form-layout.png)

5.  Search for **Token URL** from the **Available** field, add it to the **Selected** field, and move it under **Redirect URL**.

6.  Select **Save** to save the layout.![OAuth OIDC Entity form configuration page, with Token URL option selected](../images/save-form-layout-gcc-h.png)

    You’re redirected to the OAuth OIDC Entity record.

7.  On the OAuth OIDC Entity form, select the lock icon to unlock the **Token URL** field, and then update the default value:

    -   For multi-tenant application: `https://login.microsoftonline.us/MicrosoftServices.onmicrosoft.us/oauth2/v2.0/token`
    -   For Single-tenant application: `https://login.microsoftonline.us/<Tenant-ID>/oauth2/v2.0/token`
8.  Scroll down the OAuth OIDC Entity form, select the **OAuth Entity Scopes** tab, and update the OAuth scope's default value to `https://api.botframework.us/.default`.

9.  On the OAuth OIDC Entity form, select the information icon next to the **OAuth OIDC Provider Configuration** field and select **Open Record**.

10. On the OIDC Provider Configuration form, update the **OIDC Metadata URL** to `https://login.botframework.azure.us/v1/.well-known/openidconfiguration` and select **Update**.


**Parent Topic:**[Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD](../concept/va-integ-msteams-gcch.md)

