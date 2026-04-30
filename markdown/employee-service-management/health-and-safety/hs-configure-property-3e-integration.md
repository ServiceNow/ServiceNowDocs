---
title: Configure the property for 3E integration
description: Configure the property that enables retrieving safety data sheets, SOP’s and other metadata from the 3E database to the chemical library. This property enables users to have the necessary safety information before they use the chemical.
locale: en-US
release: zurich
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-11-28"
reading_time_minutes: 1
breadcrumb: [3E integration, Integration with third party services, Health and Safety, Employee Service Management]
---

# Configure the property for 3E integration

Configure the property that enables retrieving safety data sheets, SOP’s and other metadata from the 3E database to the chemical library. This property enables users to have the necessary safety information before they use the chemical.

## Before you begin

Role required: sn\_hs\_env.admin

## About this task

The \[sn\_hs\_connector\_co.3e\_source\] property value is the unique identifier for your organization in the 3E system. It must be set accurately to confirm correct data retrieval. Before configuring integration, confirm that your organization has purchased or acquired the 3E web services API license. This license provides the value to be entered in this field to access 3E APIs. These credentials enable secure communication between your application and the 3E database.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  In the **3E API call require ‘’Source’’ as mandatory field to be passed to API to unique identify client account. Default value is set to ‘’CS”** field, enter the unique identifier value for your organization.

    The value entered here acts as the customer system identifier from 3E.

3.  Select **Save**.


**Parent Topic:**[Integration of 3E with Health and Safety Environmental Management](../concept/hs-integration.md)

