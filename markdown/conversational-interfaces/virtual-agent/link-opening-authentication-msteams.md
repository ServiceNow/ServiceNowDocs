---
title: Configure link authentication and opening experience in Microsoft Teams
description: Link authentication and opening experience in Microsoft Teams provides a seamless experience for end users to interact with ServiceNow links when you use Virtual Agent on Microsoft Teams.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure VA for Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure link authentication and opening experience in Microsoft Teams

Link authentication and opening experience in Microsoft Teams provides a seamless experience for end users to interact with ServiceNow links when you use Virtual Agent on Microsoft Teams.

## Before you begin

Role required: virtual\_agent\_admin or admin

Ensure that your Microsoft Teams integration is available in the All Integrations tab of the Channels and integrations page before enabling link authentication.

Ensure that your  Microsoft Teams email ID matches with one of the system users' email.

Ensure that you are in the  Conversational Integration with Microsoft Teams scope while completing this step \(instead of the Global scope\)​.

## About this task

To configure smart links to open in a pop-up or Microsoft Teams tab, admins must first complete the following link authentication steps before moving on to configure smart links.

**Note:** When the status of link authentication is inactive, the link opening behavior falls back to New Browser Tab even when admins configure a link to be opened in a pop-up or Microsoft Teams tab. Therefore, activating link authentication is a pre-requisite of using a pop-up and Microsoft Teams tab.

**Important:** Be informed that Smart Links do not work for Now Virtual Agent if your instance has a custom domain.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and routing**, select **View All**.

3.  On the Channels and integrations page, in the Microsoft Teams tile, select **Manage**.

4.  In the Manage Microsoft Teams channel page, select the **Settings** tab.

5.  In the Enable Link Authentication section, under **Step 1. Configure SSO for tenant**, select the **Configure SSO** ![Enables Single Sign-On.](../images/enable-sso-button.png) button.

    The Single Sign-On \(SSO\) Configuration pop-up opens to inform you that the link directs you to a page to install your tenant and authorize it for SSO. Select **Open**.

    ![SSO Configuration opening dialog box.](../images/msteams-sso-confirm.png)

    For more information about configuring Single Sign-On, see [Grant permissions to required Microsoft Azure apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/authorize-multi-tenant-apps-mt.md).

    **Note:**

    -   SSO can only be enabled on one Microsoft Teams tenant at any given time. If SSO is already enabled on another tenant, make sure to switch the tenant so that SSO can be enabled on the new tenant.​
    -   If you have already configured a tenant and would like to change it to another tenant, then you can do so by selecting **Change tenant**. Once you confirm to change the tenant, you are directed to the Microsoft Teams login page for changing the tenant.
    After entering the tenant information, ensure that you have selected the **Authenticate** button in the SSO section.![Install Azure Apps portal showing SSO is installed.](../images/configure-sso-msteams.png)

6.  After you have configured SSO, you must enter an APP ID.

    To Find your APP ID, log into the [Microsoft Teams admin center](https://admin.teams.microsoft.com/policies/manage-apps), navigate to **Manage apps**, select the app you'd like to configure, and fetch the app ID.

    ![Microsoft Teams Admin Center portal open to Manage Apps tab, with App ID highlighted.](../../conversational-interfaces/image/app-ID.png)

    **Note:** If you are using ServiceNow for Teams app, search for the app ID for ServiceNow for Teams and make sure not to use External App ID.

7.  On the Link Authentication section, at **Step 2. Enter App ID**, enter the app ID that you fetched from your Microsoft Teams admin center, and select **Save**.

    You receive a confirmation that your app ID has been saved successfully. You notice that the status of against SSO is green.


-   **[Configuring smart links in Microsoft Teams](../concept/va-teams-sso.md)**  
Configure smart links for your Virtual Agent app in Microsoft Teams to enable different link opening experiences.

**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

