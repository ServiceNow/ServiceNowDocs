---
title: Set the default portal search source
description: Use the glide.service\_portal.default\_search\_sources system property to define default search sources.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Set the default portal search source

Use the **glide.service\_portal.default\_search\_sources** system property to define default search sources.

## Before you begin

Role required: admin

## About this task

If you don't define specific search sources for your portal, the system uses default search sources instead.

![Flow chart for default search sources, which shows how default search sources are only used if no search sources are defined](../image/DefaultSearchSources.png "Default search source flow chart")

## Procedure

1.  In the Navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  On the list, find the system property **glide.service\_portal.default\_search\_sources**, and then open the property record.

3.  Copy the sys\_ID of any search source you want to add into the **Value** field of the system property using a comma-separated list.

    To change the order in which the default search sources show in the Search List, change the order of the IDs in the property.

    You can remove the default search source behavior by deleting the property value or deleting the property altogether.

4.  Click **Update**.


**Parent Topic:**[Zing search in Service Portal](../concept/zing-search-service-portal.md)

