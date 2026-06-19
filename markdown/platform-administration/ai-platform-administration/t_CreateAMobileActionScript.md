---
title: Create a push action
description: A push action is a server-side script that runs when the instance receives a response to an actionable push message.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/t\_CreateAMobileActionScript.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Push notification setup with a custom push application for ServiceNow mobile apps, Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a push action

A push action is a server-side script that runs when the instance receives a response to an actionable push message.

## Before you begin

Complete the following:

1.  [Activate push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_ActivatePushNotifications.md)
2.  \(iOS only\) [Upload a push certificate to your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/upload-push-cert.md)
3.  [Create a push application record for your custom app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAMobileApplication.md)
4.  [Create push message content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAMobileMessageLayout.md)
5.  [Create a push message attribute definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAPushMessageAttribute.md)
6.  [Create an attribute value or action for a push message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAPushMessageAttributeValue.md)

Role required: admin or push\_admin

**Note:** This process describes configuration used in the ServiceNow mobile app. Push Notification configuration for the current ServiceNow mobile UI can be found at Mobile push notifications

## About this task

Create a push action to perform an action on the instance. For example, you might have an actionable push message that lets the user approve a change request. The action that handles the response should update the **Approval** field on the relevant Change Request record.

You can use global variables or, optionally, current variables and parameters passed through the [JSON content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAMobileMessageLayout.md).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Action**.

2.  Fill in the form fields \(see table\).

3.  Click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a descriptive name for the action.|
    |Script|Enter the script.|


