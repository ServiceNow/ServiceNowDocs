---
title: Configure knowledge bases
description: Enable users to view knowledge articles from the mobile app. If no knowledge bases are selected, users can view articles from all knowledge bases in the system. By default, the app uses the IT knowledge base.
locale: en-US
release: australia
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Now Mobile, Unified Employee Experience, Employee Service Management]
---

# Configure knowledge bases

Enable users to view knowledge articles from the mobile app. If no knowledge bases are selected, users can view articles from all knowledge bases in the system. By default, the app uses the IT knowledge base.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Now Mobile App** &gt; **Knowledge Bases**.

2.  In the portal knowledge bases \[m2m\_sp\_portal\_knowledge\_base\] table, add a knowledge base in addition to the IT knowledge base.

    1.  Click **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Active|Option that you can select to make the configuration active.|
        |Portal|Portal that you select. Select **Mobile Employee Service Portal**.|
        |Knowledge Base|Knowledge base that you would like to associate with the app.|
        |Order|Number that indicates the order that the configurations should run. If there are multiple configurations on a portal, the system runs the configurations from the lowest to the highest order that you selected.|

3.  Change the default knowledge base that is associated with the Now Mobile app.

    1.  In the **Portal** field, open the record with **Mobile Employee Service Portal**.

    2.  In the **Knowledge Base** field, select the knowledge base that you would like to associate with the app.

    3.  Click **Update**.


## Result

Users can select the ![Plus icon](../image/more-items.png) icon on the applet launcher page to open the quick action.

**Parent Topic:**[Configuring Now Mobile](../concept/setup-mobile-employee.md)

