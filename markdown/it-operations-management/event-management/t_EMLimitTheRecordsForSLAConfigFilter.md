---
title: Limit the records for the SLA configuration filter
description: If too many records are returned by the SLA configuration filter, you can add a property to set the maximum number of records.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an SLA configuration for CIs, SLAs for application services and CIs, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Limit the records for the SLA configuration filter

If too many records are returned by the SLA configuration filter, you can add a property to set the maximum number of records.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

By default, the size of dynamic CI group records is limited to 10,000 elements. Exceeding this limit can affect system stability. If the filter configuration for a specified dynamic CI group returns too many records, you can limit the number of records that are returned by setting the value of the sa.qbs.max\_num\_of\_cis property. For more information, see [Create a Dynamic CI Group](https://www.servicenow.com/docs/access?context=create-it-services&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Enter `sys_properties.list` in the application navigator.

2.  Add the following property:

    **sa.qbs.max\_num\_of\_cis**

3.  Set the value to an integer that represents the maximum number of records to return.


**Parent Topic:**[Create an SLA configuration for CIs](t_EMCreateAnSLAConfiguration.md)

