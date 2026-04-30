---
title: Rate limiting policy for SMS Authentication
description: Rate limiting policy locks out a user when an invalid or incorrect Soft PIN is entered consecutively for 3 times in a span of 24 hours.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure SMS authentication, Integrating Virtual Agent with Twilio, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Rate limiting policy for SMS Authentication

Rate limiting policy locks out a user when an invalid or incorrect Soft PIN is entered consecutively for 3 times in a span of 24 hours.

## Rate limiting policy

Rate limiting policy is enabled by default for SMS for better security. To configure it, navigate to **All**, and then enter `sys_cs_provider.list` in the filter. Open the SMS record, and configure the following properties on the **Provider Properties** tab.

-   **softpin\_lockout\_enabled**: Enables Soft PIN lockout functionality. The default Value is **true**.
-   **softpin\_max\_invalid\_attempts\_interval\_hrs**: The window where users can make the maximum Soft PIN attempts.

    **Note:** The maximum window is **24** hours.

-   **softpin\_max\_retry\_attempts**: Number of attempts for the user to enter an incorrect Soft PIN after the user account is locked out.

    **Note:** The maximum number of attempts is **3**.

    If your account is locked, you are treated as a guest user when you start a new conversation. The bot confirms that your account is locked. You are then provided with the public topics and you can also unlock the account using the **Setup/Reset Verification Profile** Virtual Agent topic to reset the Soft PIN and Google authenticator.


![The Provider Properties tab lists entries for each of these parameters, including the value and description.](../images/sms-auth-rate-limit-properties.png)

**Parent Topic:**[Configure SMS authentication](../task/configure-sms-auth.md)

