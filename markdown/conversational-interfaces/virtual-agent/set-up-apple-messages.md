---
title: Set up the integration on Apple Messages for Business
description: To integrate Apple Messages for Business with your ServiceNow instance, you need to set up your Apple Messages for Business account, and then link your Apple Messages for Business messaging service provider account to your ServiceNow instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Conversational Integration with Apple Messages for Business, Conversational Integration with Apple Messages for Business, Integrating Virtual Agent with consumer messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up the integration on Apple Messages for Business

To integrate Apple Messages for Business with your ServiceNow® instance, you need to set up your Apple Messages for Business account, and then link your Apple Messages for Business messaging service provider account to your ServiceNow® instance.

## Before you begin

-   Role required: admin
-   If your business doesn't already have an Apple ID, create one. Make sure to use the ServiceNow® Messaging Service Provider \(MSP\).

    **Note:** For more information about creating a business Apple ID, refer to the [Apple documentation](https://support.apple.com/guide/apple-business-manager/use-managed-apple-ids-axm78b477c81/web).

-   Create a Apple Messages for Business account.

## Procedure

1.  Go to [Apple Messages for Business](https://register.apple.com/messages) \(register.apple.com\).

2.  Click **Messages for Business Accounts** to go to your business account.

3.  Click **Test your Messaging Service Provider connection**, and **Connect**.

    You are redirected to your Now Support portal. Log in if necessary.

4.  On your Now Support portal, complete the connection of your Apple Messages for Business account with your ServiceNow instance.

    1.  Use the dropdown to select the instance that you want to connect to your Apple Messages for Business account.

        Ensure that the instance has the Conversational Integration with Apple Messages for Business application installed.

    2.  If the connection is successful, the message "Your request on the instance &lt;instance name&gt; is successfully submitted" displays.

        If the connection is not successful, you are redirected to the landing page on Now Support. Try again by repeating the connection steps.

5.  Once the connection is complete, click **Go to instance** to go to your customer instance and log in if necessary.

6.  On the Apple Messages for Business account page, enter the Provider Application name.

    This should be a name that will help you identify this connection on your instance.

7.  Click **Complete installation**.

    If the installation was successful, you are redirected to the instance homepage and the following message displays: “Bot registration successful. View the provider record here.”


## What to do next

If you want to integrate your Identity Provider \(IdP\), go to: [OAuth setup for Apple Messages for Business](oauth-setup-apple.md).

