---
title: Configure a schedule content template for a lifecycle event activity
description: Create or modify a schedule content template to deliver content as part of a lifecycle event. Each template must be associated with the Schedule Content \[sn\_cd\_content\_visibility\] table, and you can configure the template for mobile content, portal content, notification content, or to-do content.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the supporting components for a lifecycle event, Building a lifecycle event, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure a schedule content template for a lifecycle event activity

Create or modify a schedule content template to deliver content as part of a lifecycle event. Each template must be associated with the Schedule Content \[sn\_cd\_content\_visibility\] table, and you can configure the template for mobile content, portal content, notification content, or to-do content.

## Before you begin

Have the content that you want to use with the schedule content template. You can use the following types of content:

|Content type|Description|
|------------|-----------|
|[Configure mobile content](../../employee-center/task/ecpro-content-delivery-mobile.md)|Mobile content is delivered as a mobile banner in the Now Mobile and Mobile Onboarding apps.|
|[Content Publishing](../../employee-center/concept/ec-publish-content.md)|Portal content is delivered as content \(such as a banner, calendar, or video\) in a portal such as the Employee Service Center.|
|[Notification content](../../employee-center/concept/ec-notification-content.md)|Notification content is delivered as a notification.|
|[Creating to-do content that appears in a banner or styled content](../../employee-center/concept/ecpro-content-to-dos.md)|To-do content is delivered as a to-do in both portal and mobile.|

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Templates**.

2.  Click **New** or open a record.

3.  Fill in the following fields on the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the template.|
    |Table|Set the value to `Schedule Content [sn_cd_content_visibility]`.|
    |Short description|Short description of the template.|

4.  From the **Template** field, add the **Content** field.

5.  For the **Content** field, select a content record to use with the template.

6.  Add additional fields with corresponding values, as needed.

    Depending on the content type, you must add additional fields with corresponding values. Content is one of the following types.

    -   Mobile content
    -   Portal content
    -   Notification content
    -   To-do content
    For a list of the available fields for each content type, see [Schedule content](../../employee-center/concept/ec-content-publishing-schedule.md).

7.  Click **Submit** or **Update**.


## What to do next

Use the schedule content template to deliver content as part of a lifecycle event. See [Configure a lifecycle event activity for content](configure-hr-lifecycle-event-activity.md#) for more information.

**Parent Topic:**[Configure the supporting components for a lifecycle event](../concept/configure-supporting-components-for-lifecycle-event.md)

