---
title: Create and associate a location to a consumer profile
description: Create a location and associate it with the consumer profile in the Customer Service Management \(CSM\) application. With this functionality, you can create and associate multiple addresses to a consumer profile that serve other purposes.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Associating locations to consumer profiles, Creating multiple consumer profiles for a user, Configure consumers, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create and associate a location to a consumer profile

Create a location and associate it with the consumer profile in the Customer Service Management \(CSM\) application. With this functionality, you can create and associate multiple addresses to a consumer profile that serve other purposes.

## Before you begin

Role required: admin

## About this task

Here's an example of why a user created and associated a location to the consumer profile. In the Healthcare and Life Sciences industry, clinicians can store multiple addresses for a patient profile, like mailing addresses for sending reports and home addresses for sample collections.

## Procedure

1.  In the navigation filter, enter `sn_csm_consumer_profile_location_list.do`.

2.  In the Consumer Profile Locations record, select a consumer profile.

3.  In the **Location** field, select the lookup icon ![Lookup icon.](../image/search_icon.png) to open the list of locations.

4.  In the Consumer Profile Locations record, select **New**.

5.  On the form, fill in the fields.

    **Note:** Ensure that you fill in the **Consumer** field in the Location form. If the **Consumer** field is empty, you get an error.

6.  Select **Submit**.

    **Note:** If multiple consumer profile location records are associated with the location, you can't delete a location record.

    A new address is created and added to the **Location** field. You can associate this location to the consumer profile. For a description of the field values, see [Consumer Profile Location table](../reference/consumer-profile-location-table.md).

7.  Select **Update**.


**Related topics**  


[Associate an existing consumer location with a consumer profile](assoc-existing-consumer-loc.md)

