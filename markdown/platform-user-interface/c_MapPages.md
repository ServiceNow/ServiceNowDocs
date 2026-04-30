---
title: Map pages
description: Map pages display ServiceNow data graphically on a Google map page based on location data that you provide.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Map pages

Map pages display ServiceNow data graphically on a Google map page based on location data that you provide.

You can create as many map pages as required to define the types of data to display, the links to show, and the appearance of the map. After creating the map pages, you can create modules to display the map pages.

**Note:** Map pages are subject to the non-production access limitations. See [Set up Google Maps API](../task/set-up-google-maps-api.md) for details.

## Map locations

Locations are used by various applications to locate users, facilities, or configuration items \(CI\) and are stored in the Location \[cmn\_location\] table. You can configure different levels of location in a parent-child hierarchy. For example, an email server might be associated with a location of Second Floor, whereas the email business service might be associated with New York City.

Each level of this hierarchy contains a separate location record, with the next higher level specified as a parent. In this example each location is selectable as a hierarchy from reference fields:

![The Location hierarchy view](../image/LocationHierarchy1.png "Location hierarchy")

The location is also used to generate a full identifier in the **Full name** field, which is available by configuring the form. For more information, see [Show or hide fields on a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&section=t_ConfigureAForm&ft:locale=en-US).

![](../image/LocationFullName.png)

## How locations are defined

To create a location, navigate to **User Administration** &gt; **Locations** and select **New**.

<table id="table_xqf_tdw_dp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the location. This name is the display value that the system uses when referencing this location on a form.

</td></tr><tr><td>

Street

</td><td>

The street address of the location.

</td></tr><tr><td>

City

</td><td>

The city of the location.

</td></tr><tr><td>

State / Province

</td><td>

State or province of the location.

</td></tr><tr><td>

Zip / Postal Code

</td><td>

The zip or postal code of the location.

</td></tr><tr><td>

Country

</td><td>

The country of the location.

</td></tr><tr><td>

Contact

</td><td>

Name of a user who is the contact for this location.

</td></tr><tr><td>

Phone

</td><td>

The phone number for the location.

</td></tr><tr><td>

Fax phone

</td><td>

The fax number for the location.

</td></tr><tr><td>

Parent

</td><td>

Name of the parent location for this location. Location hierarchies are described above.

</td></tr><tr><td>

Latitude

</td><td>

The latitude of the location.The **get\_lat\_long** business rule automatically populates this field and the **Longitude** field described below when the form contains enough information, such as an address or city name and a postal code.

 Deactivate this business rule to avoid the system overwriting any values entered manually into these fields.

</td></tr><tr><td>

Longitude

</td><td>

The longitude of the location.

</td></tr><tr><td class="sub-head" colspan="2">

Fields that can be added by configuring the form:

</td></tr><tr><td>

Company

</td><td>

A reference field to the **Company** `[core_company]` table.

</td></tr><tr><td>

Full name

</td><td>

A read-only, calculated field that assembles the parent hierarchy of the location into a full name.

</td></tr><tr><td>

Stock room

</td><td>

A boolean field that identifies whether the location is being used as a stock room.

</td></tr><tr><td>

Time zone

</td><td>

The time zone of the location. By default, the location uses the system time zone.

</td></tr></tbody>
</table>## Latitude and longitude

When a **Company** or **Location** record is created, or has one of its address fields changed `[street, city, state, zip or country]`, the **get\_lat\_long** business rule is triggered. This business rule uses the **GoogleMapsHelper** script include to create `sys_geocoding_request` records.

The scheduled job **Process Geocoding Request** must be enabled to process `sys_geocoding_request` records. **Process Geocoding Request** uses the Google Map service to populate the latitude and longitude fields of the changed or created **Company** and **Location** records.

After the latitude and longitude are populated, Map Pages can be defined that display locations in an interactive map.

**Note:** Latitude and longitude are expressed as a floating point data type. Previous releases expressed this information as a string. During an upgrade, the system converts the data where possible.

-   **[Set up Google Maps API](../task/set-up-google-maps-api.md)**  
You enable the geolocation feature using the appropriate entries from a Google Maps API for Business license, or a Google Maps JavaScript API Key.
-   **[Create a map page](../task/t_CreateAMapPage.md)**  
Your ServiceNow instance provides several default map pages. You can also create custom map pages with the script examples described in this page.
-   **[Create a map page module](../task/create-map-page-module.md)**  
You can create a new application module for desktop or smartphone users to display a Google map page.
-   **[Create an advanced Map Page](../task/create-advanced-map-page.md)**  
Use advanced configuration to set up Map Pages without scripting.
-   **[Set map application scope](../task/set-map-application-scope.md)**  
Enable map application scope to specify which application can modify your Map Page configuration.
-   **[Create a smartphone map page module](../task/t_CreateASmartphoneMapPageModule.md)**  
You can create a custom smartphone module that links directly to a map page.
-   **[Scripting for map pages](../reference/scripting-for-map-pages.md)**  
The Script field on the Map Page form allows the use of attributes or custom code to define map characteristics, such as marker appearance, display information, and more.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

