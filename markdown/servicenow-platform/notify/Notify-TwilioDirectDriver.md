---
title: Notify Twilio Direct driver
description: The Notify-Twilio integration with the Notify-Twilio Direct driver provides APIs and workflow activities for applications to handle various notification features.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Explore, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Notify Twilio Direct driver

The Notify-Twilio integration with the Notify-Twilio Direct driver provides APIs and workflow activities for applications to handle various notification features.

The Notify-Twilio Direct driver provides the following notification features:

-   Start and manage a conference
-   Send and receive SMS messages
-   Send and receive calls

Notify automatically creates a TwiML application in the Twilio account and configures the application to use the instance as an endpoint.

Phone numbers associated with the Twilio account are imported to Notify. To manage phone numbers per instance, set up one Twilio account for each instance and configure all relevant phone numbers for the instance under that account.

**Note:** Only one Twilio account \(or subaccount\) can be configured on a given Notify driver at a time. Both the old and new driver can be used simultaneously because they can be configured with different accounts.

The Notify-Twilio direct driver supports the use of API Keys and API Secret to make outbound REST API calls to Twilio. For more details, see [API Key Resource](https://www.twilio.com/docs/iam/keys/api-key).

To enhance the security, another set of user credentials are added in the system for the credentials in the form of Twilio API keys. The record contains the generated API key and the API secret as the username and password respectively.

**Note:** Twilio Direct creates the Standard type API keys.

If the instance is connected to Twilio and you upgrade to Xanadu, the Twilio will not be disconnected from your instance and continues to use the Account SID and Auth key. However, if the administrator disconnects Twilio from the instance and re-connect the Twilio service, the additional record will be created to enhance the security.

## Activation Information

For new customers, only the Notify-Twilio Direct driver is available by default. For customers upgrading to the latest version, both the Notify-Twilio Direct and Notify-Twilio drivers are available.

The Notify plugin must be active to access Notify.

**Parent Topic:**[Exploring Notify](exploring-notify.md)

**Related topics**  


[Configure Notify with Twilio](../task/t_ConfigureNotifyWithTwilio.md)

