---
title: Configure search for places in crisis map
description: Set the system property to manage searching places on the crisis map.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up the crisis map, Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure search for places in crisis map

Set the system property to manage searching places on the crisis map.

## Before you begin

Role required: Administrator

## About this task

To enable crisis map functionality in the GRC: Crisis Map application, you must set up Google maps. For more information, see [Set up Google Maps API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/set-up-google-maps-api.md).

**Note:** Prior to enabling the Crisis Map feature, confirm that you have purchased and set up Google Maps API.

## Procedure

1.  To open the System Properties table \[sys\_properties\], enter sys\_properties.list in the left pane of the application navigation filter.

2.  Search for sn\_bcm\_map.use\_google\_places\_lib in the **Name** column.

3.  To search places in the Google map, set the value to **True** in the **Value** column for the sn\_bcm\_map.use\_google\_places\_lib system property.


