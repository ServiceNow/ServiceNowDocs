---
title: Create a Custom Map Provider record
description: Configure map providers to identify buildings agents can view indoor maps for.
locale: en-US
release: zurich
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Site Mapping for Field Service Management, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Create a Custom Map Provider record

Configure map providers to identify buildings agents can view indoor maps for.

## Before you begin

Ensure Indoor Maps are set up. For more information, see [Indoor Mapping](https://www.servicenow.com/docs/access?context=Indoor-mapping&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Site Mapping** &gt; **Custom Map Providers**.

2.  Select **New**.

3.  On the form, fill in the fields.

    **Note:** Ensure the current **Application** is **Indoor Mapping**.

    |Field|Description|
    |-----|-----------|
    |Key table|Table that contains the building values.|
    |Key|The specific building entry from the key table.|
    |Map provider|The map provider you’re using.|

4.  Select **Submit**.


## Using demo data to create a Custom Map Provider for Building A

Allie is an administrator who wants to configure Site Mapping for Field Service Management. During configuration, they install demo data to practice the procedure.

They navigate to the Custom Map Provider form and enter the following values:

|Field|Value|
|-----|-----|
|Key table|Building \[sn\_map\_core\_building\]|
|Key|Building A|
|Map provider|ServiceNow|

After submitting the form, Allie proceeds to set the new record as the provider for the Custom Map Screen.

## What to do next

The new record must be set as the default provider for the Custom Map Screen for agents to see the building on their Mobile Agent application. For more information, see.

