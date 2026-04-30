---
title: Configure the maximum number of records returned for list UI parameters
description: To configure the maximum number of records returned for a list of parameters, add the system property glide.sg.list.max\_items\_number.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile system property configurations, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the maximum number of records returned for list UI parameters

To configure the maximum number of records returned for a list of parameters, add the system property **glide.sg.list.max\_items\_number**.

## Before you begin

Role required: admin

## About this task

Default is 1000.

**Note:** The maximum number of rows returned for a parameters list is limited by the maximum number of rows returned for data items. In other words, the value for system property **glide.sg.list.max\_items\_number** cannot be greater than the value for system property **glide.sg.data\_item.row\_count**. For example, if you set the value of **glide.sg.list.max\_items\_number** to 50 but the value of **glide.sg.list.max\_items\_number** is 20, then you may only receive 20 records in your parameters list.

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Open the record for **glide.sg.list.max\_items\_number**.

3.  In the form, match the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.sg.list.max\_items\_number**|
    |Type|string|
    |Value|&lt;maximum-number-of-parameters-items&gt;|


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)

