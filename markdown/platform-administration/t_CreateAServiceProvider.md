---
title: Create a service provider
description: Administrators can configure service providers for devices that use SMS.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Subscription-based notifications, Setting notification preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a service provider

Administrators can configure service providers for devices that use SMS.

## Before you begin

Role required: admin

## About this task

**Important:** Service providers such as AT&amp;T and Verizon may soon be deprecating the **email-to-text** functionality. See [Using Notify with SMS](https://www.servicenow.com/docs/access?context=c_NotifySMS&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for SMS delivery.

Administrators also have the option of configuring how a device's service provider affects the construction of the device's email address.

## Procedure

1.  Navigate to the Notification Service Provider \[cmn\_notif\_service\_provider\] table by entering `cmn_notif_service_provider.list` in the application navigator filter.

2.  Fill out or change the fields on the form \(see table\).

3.  Select **Update**.

4.  Select **Save** on the Notification Preferences page.

<table id="table_fhh_d32_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Configured name of the service provider.

</td></tr><tr><td>

Type

</td><td>

Type of device, in this case **SMS**.

</td></tr><tr><td>

Active

</td><td>

Enables or disables this notification device.

</td></tr><tr><td>

Advanced notification

</td><td>

Removes all the previous options and displays the **Advanced script** field.

</td></tr><tr><td>

Advanced script

</td><td>

Used for custom notifications that run a script rather than construct a traditional SMS/email. This is used when all outbound SMS messages must run through a central SMS hub, as opposed to being sent directly from the instance to the SMS provider. Advanced users can construct a script in this field that will send a notification to an old style numeric pager that can’t receive SMS communications. This field is rarely used and employs advanced scripts. Contact your representative to assist you with any advanced SMS scripting.

</td></tr><tr><td>

Construct address manually

</td><td>

Removes the prefix and suffix options and displays the **Construction script** field.

</td></tr><tr><td>

Construction script

</td><td>

Enables you to script the email address construction as you would in a business rule. For example, `abc + current.phone_number + def@text.att.net` would construct an email address of `abc2223334444def@text.att.net`.**Note:** `Current` is a reference to the device, not the service provider, therefore the *current.phone\_number* variable that uses the device's `phone_number` value.

</td></tr><tr><td>

SMS Provider Email Prefix

</td><td>

Places the provided text before the device's specified phone number; for example: `PREFIX2223334444@text.att.net`

</td></tr><tr><td>

SMS Provider Email Suffix

</td><td>

Places the provided text after '@' sign; for example: `2223334444@SUFFIX`

</td></tr><tr><td>

Notification Device Variables

</td><td>

Optional attributes of an SMS device used inside an SMS service provider's **Advanced script**. This is used to deliver SMS notifications to an internal SMS distribution technology. This is an advanced scripting procedure and isn’t necessary for configuring external SMS providers.

</td></tr></tbody>
</table>
-   **[Select a service provider](t_SelectingAServiceProvider.md)**  
You can configure how a device's service provider affects the construction of the device's email address.
-   **[SMS notification advanced scripting](../reference/r_SMSNotificationAdvancedScripting.md)**  
You can use these objects and their attributes in your advanced notification scripts on the SMS Notification Service Provider form.

**Parent Topic:**[Subscription-based notifications](../concept/c_SubscriptionBasedNotifications.md)

