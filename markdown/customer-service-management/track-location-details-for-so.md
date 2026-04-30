---
title: Tracking the location details for a service organization
description: By tracking and capturing the location details for a service organization, you can provide Field Service Management, Walk-up Experience and appointment booking capabilities.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a business location, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Tracking the location details for a service organization

By tracking and capturing the location details for a service organization, you can provide Field Service Management, Walk-up Experience and appointment booking capabilities.

## Location tracking details

You can provide Field Service Management, Walk-up Experience, and appointment booking capabilities through the service organization data model by capturing the Location \(cmn\_location\) table details.

**Note:** You must activate the service organization \(com.snc.service\_organization\) plugin before you can track the location details for a service organization.

## Location field

By going to the service organization form, you can see that there's a **Location** field, where you can add the information about your geographical location, that is, the cmn\_location of the service organization. The address fields on the cmn\_location table is synchronized with the service organization but not the vice versa.

**Note:** Changes to the cmn\_location record don’t update the address fields on the service organization.

The address fields on the service organization record that are synchronized with the location \(cmn\_location\) include:

-   Street
-   City
-   State
-   Country
-   Zip / Postal Code
-   Latitude
-   Longitude

**Note:** With the base system, the Location fields don’t appear on the form or list views. If the location field on the service organization isn’t defined, an on-demand script is shipped with the base system. The script generates the cmn\_location record from the address fields.

