---
title: Create a push action
description: Create push actions to suit your needs, when the base system actions do not meet your requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/mobile-platform/actionable-push-notification-2-3.html
release: zurich
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure actionable push notifications, Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Create a push action

Create push actions to suit your needs, when the base system actions do not meet your requirements.

## Before you begin

Role required: admin

## Procedure

1.  In the web-based UI, enter `sys_sg_push_action.list` in the filter navigator to open the push action categories list.

    \[Omitted image "open-action.png"\] Alt text: Use the filter navigator to open the push action category list

2.  In the push action categories list, click **New**.

3.  On the push action form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Label for the push action. This is the text your users will see in the notification for this action.|
    |Application|The scoped application for this record. This field automatically populates.|
    |Name|Name of the push action|
    |Foreground|When enabled, the app will open when your users select this action.|
    |Response Type|Select **Simple** or **Text response**. Actions using **Text response** prompt your users to enter text before completing the action.|
    |Placeholder Text|Text displays as a placeholder text to your users when they initiate the actionable push.|

4.  Click **Save**.


**Parent Topic:**[Configure actionable push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/actionable-push-notification.md)

