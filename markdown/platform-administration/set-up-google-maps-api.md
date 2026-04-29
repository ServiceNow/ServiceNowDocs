---
title: Set up Google Maps API
description: You enable the geolocation feature using the appropriate entries from a Google Maps API for Business license, or a Google Maps JavaScript API Key.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up Google Maps API

You enable the geolocation feature using the appropriate entries from a Google Maps API for Business license, or a Google Maps JavaScript API Key.

## Before you begin

Role required: admin

## About this task

You can generate maps using basic JavaScript, and they are flexible enough to display even the most complicated of queries. These maps use standard Google Maps API for Business or Google Maps JavaScript API Key mapping features, including various link types to records in your instance. Use of this feature requires installation of the Google Maps plugin.

![Map page](../image/MapPage.jpg "Map page")

**Important:** Starting May 2026, Google is deprecating the use of Client ID for authenticating requests to Google Maps. From this date onward, API keys will be the only supported authentication method. If your application continues to use client-id \(for example, via the **google.maps.method property**\), Google Maps requests will fail. For more information, see [Client ID Migration Guide](https://developers.google.com/maps/premium/migrate-client-id).

Update your configuration to authenticate using an API key only \(that is, set **google.maps.method** to `key`\). Refer to the descriptions of **google.maps.key** and **google.maps.key.geocoding** properties for more information on API key–based authentication.

## Procedure

1.  Google Maps APIs for Business licenses are no longer available from Google, so, depending on whether have an existing license, use one of the following procedures.

    **Note:** You are required to use your own Google Maps JavaScript API Key from Google and not use any ServiceNow AI Platform® generated key.

<table id="choicetable_okq_vnj_smb"><thead><tr><th align="left" id="d106103e127">

Existing Google Maps API for Business license available?

</th><th align="left" id="d106103e133">

Tasks

</th></tr></thead><tbody><tr><td id="d106103e139">

**Existing license available**

</td><td>

1.  In the **System Properties** &gt; **Google Maps** property form:
    -   In the **google.maps.client** field,enter the Client ID for your organization. This ID is from Google and starts with `gme-`, such as `gme-mycompanyname`.
    -   In the **google.maps.client.key** field, enter the private key for Google Maps API for Business. An example of an encoded key is `vNIXE0xscrmjlyV-12Nj_BvUPaw=`. The ServiceNow AI Platform® requires this key to retrieve accurate driving time estimates from Google for some Geolocation features.
    -   Fill out the remaining values on the form.
2.  Configure your maps using the property definitions from the table.
 **Important:**

The Google Maps Client ID–based configuration is being deprecated. Client ID authentication will not be supported starting May 2026, and configurations relying on it will no longer work.

</td></tr><tr><td id="d106103e213">

**No license available**

</td><td>

1.  Obtain a Google Maps JavaScript API Key from Google.
2.  In the **System Properties** &gt; **Google Maps** property form, enter the API key into the **google.maps.key** field.

Geolocation in the ServiceNow AI Platform® uses the API Key, which Google Maps also uses for Geolocation and map view billings.

3.  Fill out the remaining values on the form.
4.  Configure your maps using the property definitions from the table.


</td></tr></tbody>
</table>    To learn more about Google Maps API for Business, and Google Maps JavaScript API Key, see [https://developers.google.com/maps/gmp-get-started](https://developers.google.com/maps/gmp-get-started).

2.  After you complete and save the configuration, create Map pages, or use the default pages included with the plugin.

    Map pages define what data appears on the map, and the appearance of the links. For a tutorial on how to view all of the markers that link to your records, see the [Display Map Markers on Google Maps](https://community.servicenow.com/community?id=community_blog&sys_id=909ceae1dbd0dbc01dcaf3231f96192b) blog post on the ServiceNow Community.

<table id="table_edd_4zf_vt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

google.maps.method

</td><td>

Defines which method of authentication should be used for Google Maps.-   Type: string
-   Default value: key
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.auto\_close

</td><td>

If true, automatically closes a map information window before opening a new one.-   Type: true/false
-   Default value: true
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.client

</td><td>

Client ID for Google Maps API for Business.-   Type: string
-   Default value: gme-servicenow
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.map\_id

</td><td>

Map ID for Google Maps used for the cloud-based maps styling, vector maps, and advanced markers. To obtain your Map ID, see [How to create map IDs](http://developers.google.com/maps/documentation/javascript/map-ids/get-map-id).-   Type: string
-   Default value: empty
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.client.key

</td><td>

Private key for Google Maps API for Business. This key activates the geolocation feature, which locates users in the system precisely, using data from their mobile devices.-   Type: string
-   Default value: empty
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.version

</td><td>

Version number of the current installation of Google Maps API for Business.-   Type: string
-   Default value: current version number
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.key

</td><td>

Google Maps API for Business or Google Maps JavaScript API Key that ties to the URL of the server. This key authorizes development use of Google Maps API.-   Type: string
-   Default value: empty
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.key.geocoding

</td><td>

Google Maps API for business or Google Maps JavaScript API key that ties to the URL of the server. This key is used for making geocoding requests.-   Type: string
-   Default value: empty
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.latitude

</td><td>

Starting latitude of the map. This value determines the starting position displayed in Google Maps.-   Type: string
-   Default value: 36.008522
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.longitude

</td><td>

Starting longitude of the map. This value determines the starting position displayed in Google Maps pages.-   Type: string
-   Default value: -95.221764
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.max\_items

</td><td>

Maximum number of items to display on the map.-   Type: integer
-   Default value: 500
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.table

</td><td>

Table used by the map. The table needs the following fields: name, longitude, latitude.-   Type: string
-   Default value: cmn\_location
-   Location: **System Properties** &gt; **Google Maps**


</td></tr><tr><td>

google.maps.zoom

</td><td>

Starting zoom level of the map \(1 is the lowest\)-   Type: string
-   Default value: 4
-   Location: **System Properties** &gt; **Google Maps**


</td></tr></tbody>
</table>3.  Perform these configurations:

    1.  Navigate to **System Properties** &gt; **All**.

    2.  Set values for these system properties:

<table id="table_dww_kh2_r4b"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

google.maps.refresh.latlong.duration

</td><td>

Number of days after which the location details are updated.**Note:** The maximum value is 30.

</td></tr><tr><td>

google.maps.refresh.latlong.record\_count\_per\_table

</td><td>

Maximum number of records in a table that can be processed using the scheduled job in one refresh.

</td></tr></tbody>
</table>    3.  Specify the tables that store the location details in the Map Coordinates Refresh Configuration \[cmn\_coordinate\_refresh\_config\] table.

    4.  If there are no fields to track when the coordinates are last retrieved in your tables:

        1.  Create the **coordinates\_retrieved\_on** field of the type **Date/Time** in your tables.
        2.  Ensure that the value of the field that tracks time when the coordinates are last retrieved, is populated correctly in the Map Coordinates Refresh Configuration \[cmn\_coordinate\_refresh\_config\] table. Refer to the sample fix script Update coordinates updated on field to update values in the **coordinates\_retrieved\_on** field.
    5.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    6.  Open the record, **Refresh Latitude Longitude info of Records**.

    7.  Select the **Active** check box.

    8.  Specify the frequency at which the location details should be refreshed by providing frequency details in **Run** and **Repeat Interval**.

        **Note:** Ensure that you refresh the location details at least once every 30 days.

4.  To access Google Maps from the ServiceNow instance based on your region, perform these configurations.

    1.  Navigate to **User Administration** &gt; **Users**.

    2.  Select and assign the relevant **Country Code** for the required user.

        **Note:** If the required **Country Code** isn't available, add the dictionary entry. Ensure that you use the ISO 3166-1 country codes. For example, the country code of Morocco is `MA`.

    3.  Navigate to **System Properties** &gt; **Google Maps**.

    4.  Select the **Yes** check box for **Enable this property only when you want to alter the Google map's behavior based on a region. The region is populated from the current User's 'Country code' field value in sys\_user record. The Country code value on the sys\_user record should be consistent with the expectations from the Google Map's region code. Most Unicode region identifiers are identical to ISO 3166-1 codes, with some notable exceptions. Check the codes properly before making any changes.**

    5.  Click **Save**.


**Parent Topic:**[ServiceNow provided integrations](../../../integrate/vendor-specific-integrations/reference/r_ServiceNowProvidedintegrations.md)

