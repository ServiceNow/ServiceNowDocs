---
title: Integrate ServiceNow Virtual Agent with Workplace from Facebook
description: Add Virtual Agent to your Workplace from Facebook integration.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Conversational Integration with Workplace from Facebook, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate ServiceNow Virtual Agent with Workplace from Facebook

Add Virtual Agent to your Workplace from Facebook integration.

## Before you begin

Roles required:

-   virtual\_agent\_admin and external\_app\_install\_admin or admin
-   Administrator for third-party applications

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, click **View All**.

    The Channels and integrations page opens.

3.  Under the Available Channels section in the Microsoft Teams tile, click **Add Integrations**.

    **Note:** The **Add Integrations** button is available only after installing the Conversational Integration with Workplace from Facebook plugin \(sn\_va\_fb\_workplace\) on your ServiceNow instance.

    You are directed to the Workplace admin page to add a bot.

4.  On the login screen for Workplace, enter your login credentials.

    If you have multiple accounts for Workplace, a menu displays the accounts that you can log in to. Select the account in which you want to install the app.

5.  In the window that requires your authorization to install the integration, click **Add to Workplace**.

    ![Installation dialog box for Virtual Agent Integration from Workplace from Facebook.](../images/FBInstall.png)

    If the selected workspace has already been integrated with Workplace, click **Save** or **Cancel** to leave the current assignment in place.

    To delete the Conversational Integration with Workplace from Facebook, see [Uninstall the Conversational Integration with Workplace from Facebook](uninstall-virtual-agent-fb.md).

6.  When you see a confirmation message about the installation, verify the installation.

    ![Confirmation message dialog box for adding Workplace from Facebook Integration.](../images/workplace-integ-success.png)


## Result

The Virtual Agent bot and Workplace from Facebook are now integrated for use on your ServiceNow instance.

**Parent Topic:**[Configuring Conversational Integration with Workplace from Facebook](../concept/configuring-ci-workplace-fb.md)

