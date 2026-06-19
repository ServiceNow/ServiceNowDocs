---
title: Deactivate offline mode on your instance
description: Deactivate the offline mode by creating the property glide.sg.offline.enabled and setting the property to false.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/deactivate-offline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-05-31"
reading_time_minutes: 1
breadcrumb: [Install and enable, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Deactivate offline mode on your instance

Deactivate the offline mode by creating the property glide.sg.offline.enabled and setting the property to false.

## Before you begin

Role required: mobile\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Select **New** in the System Properties table.

3.  Enter `glide.sg.offline.enabled` in the **Name** field.

4.  Select **True/False** in the **Type** field.

5.  Set the **Value** field to **False**.

6.  Select **Submit**.


**Parent Topic:**[Install and enable offline capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/enable-offline.md)

