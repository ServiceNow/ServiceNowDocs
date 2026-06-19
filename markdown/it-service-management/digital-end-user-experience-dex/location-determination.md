---
title: Device location determination
description: Identify and determine the number of impacted devices based on the location by defining a custom logic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/location-determination.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Device location determination

Identify and determine the number of impacted devices based on the location by defining a custom logic.

Identify and determine the number of impacted devices based on the location by configuring a custom logic for location determination. Device location can be set using three predefined configurations. DEX administrators can select an option in the system properties and `sn_dex.location_determination`. The property controls how DEX identifies the positioning of the device used to establish the device's location \(in the cmdb\_ci\_computer table\) and throughout DEX for reporting and alerting purposes.

## default\_gateway\_determined\_location

Location determination logic: DEX uses the default gateway of the device to determine the location.

-   Identify the default gateway IP address of the device.
-   Match this gateway to the switches in cmdb\_ci\_ip\_switch.

The assigned location of the switch is identified as the device’s location. If not, the device is marked as Remote \(see Remote location format logic\).

**Note:**

When `sn_dex.location_determination` is set to `default_gateway_determined_location` to make the Geomap work on the DEX dashboard:

-   Verify that the State and Country fields in the location \(`cmn_location`\) records associated with the `cmdb_ci_ip_switch` table use standard codes that match the values in the `sys_report_map_source_mapping` table.
-   Verify that the latitude and longitude values are populated correctly in the associated location records.

## device\_user\_assigned\_location

Location determination logic: DEX prefers the device’s assigned location and falls back to the employee’s location if needed.

-   Use the device’s location from cmdb\_ci\_computer.
-   If unavailable, use the owner’s location from sys\_user.

If neither of the option is set, the device is marked as Remote \(see Remote location format logic\).

**Note:**

When `sn_dex.location_determination` is set to `device_user_assigned_location` to make the Geomap work on the DEX dashboard:

-   Verify that the state and country fields in the location records associated with the `cmdb_ci_computer` and `sys_user` tables use standard codes that match the values in the `sys_report_map_source_mapping` table.
-   Verify that the latitude and longitude values are populated correctly in the associated location records.

## geoIP\_determined\_location

`geoIP_determined_location` is the default option.

Location determination logic: DEX uses GeoIP based on network connectivity to determine the location using the GeoIP data.

When a device is marked as Remote, DEX uses GeoIP to determine the Region or State and Country. With an admin role, you can set the format \(Remote, State, Country, or Remote, Country\) in `sys_property` `sn_dex.remote_location_config`.

-   The `country` format: Remote, Country \(For example, Remote, USA\), where the country is determined by GeoIP.
-   The `include_state` format: Remote, CA, USA, where state and country are determined by GeoIP.

**Note:**

When `sn_dex.location_determination` is set to `geoIP_determined_location`, to make the Geomap work on the DEX dashboard, no manual configuration is required. DEX automatically populates the state, country, latitude, and longitude values.

**Parent Topic:**[Advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-advanced-configuration.md)

