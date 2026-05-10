---
title: Install Conversational SMS service channel
description: You can install the Conversational SMS service channel application \(sn\_awa\_sms\_int\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Install Conversational SMS service channel

You can install the Conversational SMS service channel application \(sn\_awa\_sms\_int\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   The Conversational Messaging plugin \(com.glide.messaging.awa\) must be installed.

    For more information on activating plugins, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).


Role required: admin

## About this task

**Note:** The Conversational SMS service channel is automatically installed with an application that implements an SMS provider, such as the Conversational SMS Integration with Twilio \(sn\_va\_sms\_twilio\) application. For more information, see [Install Conversational SMS Integration with Twilio](../../virtual-agent/task/install-sms-twilio.md).

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home**.

2.  In the Available Plugins section, select **Conversational SMS**.

    **Note:** If you cannot find the application, you may have to request it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select **Install**, and then in the Install dialog box, select **Install**.


## What to do next

[Set up the Conversational SMS service channel](configure-conversational-sms.md)

