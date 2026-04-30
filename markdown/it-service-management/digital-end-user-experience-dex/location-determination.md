---
title: Device location determination
description: Identify and determine the number of impacted devices based on the location by defining a custom logic.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Digital End-User Experience, IT Service Management]
---

# Device location determination

Identify and determine the number of impacted devices based on the location by defining a custom logic.

Identify and determine the number of impacted devices based on the location by configuring a custom logic for location determination. Device location can be set using three predefined configurations. DEX administrators can select an option in the system properties and `sn_dex.location_determination`. The property controls how DEX identifies the positioning of the device used to establish the device's location \(in the cmdb\_ci\_computer table\) and throughout DEX for reporting and alerting purposes.

## default\_gateway\_determined\_location

Location determination logic: DEX uses the default gateway of the device to determine the location.

-   Identify the default gateway IP address of the device.
-   Match this gateway to the switches in cmdb\_ci\_ip\_switch.

The assigned location of the switch is identified as the device’s location. If not, the device is marked as Remote \(see Remote location format logic\).

## device\_user\_assigned\_location

Location determination logic: DEX prefers the device’s assigned location and falls back to the employee’s location if needed.

-   Use the device’s location from cmdb\_ci\_computer.
-   If unavailable, use the owner’s location from sys\_user.

If neither of the option is set, the device is marked as Remote \(see Remote location format logic\).

## geoIP\_determined\_location

`geoIP_determined_location` is the default option.

Location determination logic: DEX uses GeoIP based on network connectivity to determine the location using the GeoIP data.

When a device is marked as Remote, DEX uses GeoIP to determine the Region or State and Country. With an admin role, you can set the format \(Remote, State, Country, or Remote, Country\) in `sys_property` `sn_dex.remote_location_config`.

-   The `country` format: Remote, Country \(For example, Remote, USA\), where the country is determined by GeoIP.
-   The `include_state` format: Remote, CA, USA, where state and country are determined by GeoIP.

