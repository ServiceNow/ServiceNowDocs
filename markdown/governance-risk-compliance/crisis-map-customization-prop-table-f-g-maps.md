---
title: Customization properties table for Google Maps
description: Customization properties for Google Maps are explained in the Google Maps Properties table.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customization properties, Setup for Crisis map, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Customization properties table for Google Maps

Customization properties for Google Maps are explained in the Google Maps Properties table.

<table id="table_zvp_c3y_cyb"><thead><tr><th>

Name of the customization property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Defines which method of authentication should be used for Google Mapsgoogle.maps.method

**Note:** The "Name of the customization property" column refers to the customization properties mentioned in the [Customization properties for Google Maps](../concept/crisis-map-customization-properties-for-g-maps.md) topic.

</td><td>

-   Type: choice list \(client-id,key\)
-   Default value: Key

</td></tr><tr><td>

If true, automatically closes the current "info window" before opening a new one. If false, you can have multiple "info windows" open.google.maps.auto\_close

</td><td>

-   Type: yes or no
-   If set to True, automatically closes the current info window before opening a new window.

</td></tr><tr><td>

Map key from Google, tied to the URL of the server. To obtain a new key, visit [http://www.google.com/apis/maps/signup.html](http://www.google.com/apis/maps/signup.html) for details.google.maps.key

</td><td>

**Note:** The Fam-map component uses the key \(google.maps.key\) and client ID \(google.maps.client\) set for the authentication. You must use one of the options: either the key or client-ID.

</td></tr><tr><td>

Client ID for Google Maps API for Business. To obtain your own key, visit [http://www.google.com/enterprise/earthmaps/maps.html](http://www.google.com/enterprise/earthmaps/maps.html) for details.google.maps.client

</td><td>

-   Map key from Google, tied to the URL of the server.
-   Default value: gme-servicenow

</td></tr><tr><td>

Customer provided Google Maps key used for geocoding requests. To get the key, see [https://developers.google.com/maps/documentation/geocoding/get-api-key](https://developers.google.com/maps/documentation/geocoding/get-api-key)google.maps.key.geocoding

</td><td>

-   Google Maps key used for geocoding requests.
-   Default value: None

</td></tr><tr><td>

Maximum number of items to display on the mapgoogle.maps.max\_items

</td><td>

-   Maximum number of items to display on the map.
-   Default value: 500

</td></tr><tr><td>

Table used by the map. The table requires the fields: Name, Longitude, Latitude.google.maps.table

</td><td>

-   Table used by the map.
-   Default value: cmn\_location

</td></tr><tr><td>

Google Maps Versiongoogle.maps.version

</td><td>

-   Google Maps Version
-   Default value: 3.37

</td></tr><tr><td>

Duration in the number of days. It is used while refreshing the longitude and latitude of a location saved in the system. Storing them beyond 30 days time period violates the Google maps terms and conditions. Verify that it is always set to a value less than 30.google.maps.refresh.latlong.duration

</td><td>

-   Duration in the number of days.
-   Default value: 28

</td></tr><tr><td>

Enable this property only when you want to alter the Google map's behavior based on a region. The region is populated from the current User's 'Country code' field value in sys\_user record. The Country code value on the sys\_user record should be consistent with the expectations from the Google Map's region code. Most Unicode region identifiers are identical to ISO 3166-1 codes, with some notable exceptions. Check the codes properly before making any changes.google.maps.localization.region.enable

</td><td>

-   Enable this property when you want to alter the Google Map's behavior based on a region.
-   Type: yes or no

</td></tr></tbody>
</table>**Parent Topic:**[Customization properties for Google Maps](../concept/crisis-map-customization-properties-for-g-maps.md)

