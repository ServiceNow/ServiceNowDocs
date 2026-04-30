---
title: Integrate ServiceNow Virtual Agent with Microsoft Teams
description: Add the Now Virtual Agent bot to your ServiceNow instance to integrate with Microsoft Teams.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-08-15"
reading_time_minutes: 2
keywords: [Integrate, Virtual agent, MSTeams, Microsoft, Teams, sn\_va\_teams]
breadcrumb: [Integrating ServiceNow Virtual Agent with Microsoft Teams, Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate ServiceNow Virtual Agent with Microsoft Teams

Add the Now Virtual Agent bot to your ServiceNow instance to integrate with Microsoft Teams.

## Before you begin

Ensure that you’ve installed the Conversational Integration with Microsoft Teams plugin \(sn\_va\_teams\) on your ServiceNow instance before adding any integrations.

Role required: admin

**Note:** This activity requires the Application Administrator or Global Administrator roles, but only to accept one-time permissions for the application on behalf of the customer.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, select **View All**.

    The Channels and integrations page opens.

3.  Under the Available Channels section in the Microsoft Teams tile, select **Add Integrations**.

    **Note:** The **Add Integrations** drop-down is available only after installing the Conversational Integration with Microsoft Teams plugin \(sn\_va\_teams\) on your ServiceNow instance.

    ![Microsoft Teams Add Integrations drop-down, with Integrate with ServiceNow Virtual Agent selected.](../images/add-msteams-integ.png)

4.  From the **Add Integrations** drop-down, select **Integrate with ServiceNow Virtual Agent**.

5.  In the Microsoft Pick an account screen, select a Microsoft Teams account that you would like to use for the integration.

    ![Microsoft Teams account integration selection dialog box.](../images/pick-msteams-account.png)

6.  Log in to the selected Microsoft Teams account.

7.  In the ServiceNow Virtual Agent screen, select **Accept** to accept the permissions for the app.![Logging into the Microsoft Teams account to integrate with your Now Virtual Agent requires you to accept the requested permissions.](../images/va-teams-permissions.png)

8.  If the selected tenant has already been assigned to Virtual Agent, you must first uninstall from the previously associated instance.

    **Note:** Starting from Tokyo release, if your Microsoft Teams tenant is already associated with another ServiceNow instance. If you intend to associate it with a new instance, then you're asked to contact the administrator to first uninstall it from the previously associated instance. For more information, see [Override Microsoft Teams integration](override-msteams-install.md).

    ![Microsoft Teams integration tenant association removal message.](../images/msteams-new-proceed-uninstall.png)

    Installation starts in the background. After the installation completes, a message confirms that you successfully installed the Now Virtual Agent integration for Microsoft Teams.

    ![Message indicating successful installation of the ServiceNow Virtual Agent integration for Microsoft Teams.](../images/msteams-install-success.png)

9.  Select **Go to Microsoft Teams** to manage your Microsoft Teams app.

10. Select **Continue to manage channels and integrations** to manage the integration on your ServiceNow instance.

    The Microsoft Teams application appears in the list of integrations.


## What to do next

If you would like to integrate your ServiceNow® instance with another Microsoft Teams bot, select the Add Integration for ServiceNow® Virtual Agent icon against the ServiceNow® Virtual Agent bot or select the **Add integration** drop-down on the Manage Microsoft Teams channel page.

![Manage Microsoft Teams channel view in Conversational Interfaces general settings. The Add integration for ServiceNow Virtual Agent icon and the Integrate with ServiceNow Virtual Agent add integration selection are highlighted.](../images/add-integration-icon.png)

.

For more information, see [Manage the ServiceNow Virtual Agent integration with Microsoft Teams](configure-va-teams.md).

