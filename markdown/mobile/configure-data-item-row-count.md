---
title: Configure the maximum number of records returned for data items
description: To set the maximum number of rows retrieved for the table defined in the data item, add the system property glide.sg.data\_item.row\_count.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the maximum number of records returned for data items

To set the maximum number of rows retrieved for the table defined in the data item, add the system property **glide.sg.data\_item.row\_count**.

## Before you begin

Role required: admin

## About this task

The system property **glide.sg.data\_item.row\_count** sets the maximum number of rows retrieved for the table defined in the data item. By default, the value is 500. The system accepts no value greater than 500.

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Click **New**, and then enter the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.sg.data\_item.row\_count**|
    |Type|integer|
    |Value|&lt;maximum-number-of-records-retrieved&gt;|


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)

