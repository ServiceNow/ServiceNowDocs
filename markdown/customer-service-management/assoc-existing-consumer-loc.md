---
title: Associate an existing consumer location with a consumer profile
description: Associate an existing consumer location with a consumer profile by using the Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table in the Customer Service Management \(CSM\) application. By connecting consumer profiles and locations, industries can handle multiple addresses that are associated with individual profiles.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Associating locations to consumer profiles, Creating multiple consumer profiles for a user, Configure consumers, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Associate an existing consumer location with a consumer profile

Associate an existing consumer location with a consumer profile by using the Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table in the Customer Service Management \(CSM\) application. By connecting consumer profiles and locations, industries can handle multiple addresses that are associated with individual profiles.

## Before you begin

Role required: admin

## About this task

By using the Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table, you can store the relationship between the consumer profile and location.

## Procedure

1.  In the navigation filter, enter `sn_csm_consumer_profile_location_list.do`.

2.  In the Consumer Profile Locations record, select **New**.

3.  In the **Location** field, select the lookup icon ![Lookup icon](../image/search_icon.png) to open the list of locations.

4.  Select the location to be associated with the consumer profile.

5.  On the form, fill in the fields.

    For a description of the field values, see [Consumer Profile Location table](../reference/consumer-profile-location-table.md).

6.  Select **Submit**.


## Result

A location has been added to the consumer profile. Additionally, you can include different addresses, like a mailing address or a shipping address, and associate them with the same consumer profile, depending on the use case.

**Related topics**  


[Create and associate a location to a consumer profile](creating-loc-and-assoc-to-consumer-profile.md)

