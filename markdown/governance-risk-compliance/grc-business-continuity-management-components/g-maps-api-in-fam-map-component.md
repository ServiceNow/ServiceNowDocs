---
title: Google Maps APIs used in Fam-map component
description: The Fam-map component in Crisis map utilizes various Google Maps APIs to provide interactive mapping functionalities. This section lists the Google Maps APIs that are integrated into the Fam-map component, along with their usage information.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup for Crisis map, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Google Maps APIs used in Fam-map component

The Fam-map component in Crisis map utilizes various Google Maps APIs to provide interactive mapping functionalities. This section lists the Google Maps APIs that are integrated into the Fam-map component, along with their usage information.

## Maps - Dynamic Maps JavaScript API

<table id="table_rhf_5jm_b1c"><thead><tr><th>

Product

</th><th>

Description

</th><th>

Library

</th></tr></thead><tbody><tr><td>

Maps JavaScript API

</td><td>

The Fam-map component relies on the Dynamic Maps JavaScript API to load the dynamic maps. This API enables for the dynamic creation and manipulation of the maps. It also provides a foundation for the interactive features in the component.

 For detailed documentation and pricing information, see [https://developers.google.com/maps/documentation/javascript](https://developers.google.com/maps/documentation/javascript).

</td><td>

@googlemaps/js-api-loader

</td></tr></tbody>
</table>|Features|Module|Default|Usage|
|--------|------|-------|-----|
|Markers|google.maps.Marker|Enabled|Basic|
|Marker cluster|@googlemaps/markerclusterer|Enabled|Basic|
|Custom OverlayView|google.maps.OverlayView|Enabled|Basic|
|Polyline|google.maps.Polyline|Enabled|Basic|
|Polygon|google.maps.Polygon|Enabled|Basic|
|Circle|google.maps.Circle|Enabled|Basic|
|Rectangle|google.maps.Rectangle|Enabled|Basic|
|FeatureStyleFunction|google.maps.FeatureStyleFunctionOptions|Disabled|Basic|
|Customize map style|For a list of all available values for `featureType`, `elementType`, and `stylers`, see the [https://developers.google.com/maps/documentation/javascript/style-reference](https://developers.google.com/maps/documentation/javascript/style-reference).|Enabled|Basic|

|Name|Description|Type|Required|
|----|-----------|----|--------|
|[mapProperties](https://developers.google.com/maps/documentation/javascript/reference/map#MapOptions)|Properties of Google Map to set when loading|array|No|

|Products|Description|Module|Default|Usage|
|--------|-----------|------|-------|-----|
|[Nearby Search](https://developers.google.com/maps/documentation/javascript/places#place_search_requests)|Billing depends on the fields that a user utilizes.|google.maps.places.PlacesService\(mapRef\). nearbySearch|Disabled|Basic|
|[Places Details](https://developers.google.com/maps/documentation/places/web-service/usage-and-billing?_gl=1*13aif4x*_ga*MTM2NTIzOTE3Mi4xNzAyODgwMjc4*_ga_NRWSTWS78N*MTcwNDMzNDM5Ny4xMy4xLjE3MDQzMzQ5ODEuMC4wLjA.)|Billing depends on the fields that a user utilizes.|google.maps.places.PlacesService|Disabled|Basic|
|[Autocomplete - Per request+](https://developers.google.com/maps/documentation/places/web-service/usage-and-billing?_gl=1*1rwz19i*_ga*MTM2NTIzOTE3Mi4xNzAyODgwMjc4*_ga_NRWSTWS78N*MTcwNDMzNDM5Ny4xMy4xLjE3MDQzMzU0NTMuMC4wLjA.#query-ac-per-request)|The Autocomplete – Per Request SKU is charged for any of these calls or requests that do not include a session token: JavaScript: the Maps JavaScript API’s Place Autocomplete service|google.maps.places.AutocompleteService\(\). getQueryPredictions\(\{input, language\}\)|Disabled|Basic|

**Note:** For details about the properties and handlers usage in the Geo-map component, see the Geo-map Readme file. For information on the Google Maps APIs in the Geo-map component, see the KB article: [KB1588661](https://support.servicenow.com/nav_to.do?uri=/kb%3Fid=kb_article_view&sysparm_article=KB1588661)

**Parent Topic:**[Setup for Crisis map](../concept/crisis-map-admin-tasks.md)

