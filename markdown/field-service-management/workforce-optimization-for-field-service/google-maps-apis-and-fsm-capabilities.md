---
title: Google Maps APIs for Field Service capabilities
description: Field Service requires Google Maps API configuration for users to operate location features properly.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Google Maps, Set up workforce, Configure, Field Service Management]
---

# Google Maps APIs for Field Service capabilities

Field Service requires Google Maps API configuration for users to operate location features properly.

Google allocates API licenses to enable Google Maps. FSM with geolocation requires that you set up two API keys for client and server.

Use the following table to match Google Maps APIs with FSM capabilities.

**Note:**

Google designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. For more information see, [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).

You can’t generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create new Google API keys after March 1, 2025, you must enable the new APIs from Google Console and upgrade to a supported release version to ensure compatibility. For more information on the affected versions, resolution, and compatible versions, see [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf) and [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026).

|FSM capability|Description|Corresponding Google Maps API|
|--------------|-----------|-----------------------------|
|Geolocation|The auto-routing or auto-dispatch functions need this license or JavaScript API Key to calculate precise travel time estimates. Without these values, precise driving times can’t be calculated, and it uses rough estimates or fixed times instead.|[Geocoding API](https://developers.google.com/maps/documentation/geocoding/start)|
|Map Pages|Map pages display ServiceNow data graphically on a Google map page based on the location data that you give.|[Maps Javascript API](https://developers.google.com/maps/documentation/javascript/overview)|
|Optimize Route and Show Route|Field service agents can view optimized routes for tasks assigned to them on a given day or even the map a customer sees to track the technician on the way to their house. Field service dispatchers can view optimize routes for tasks assigned to members in their assignment groups. Field service managers can view optimize routes for tasks assigned to members in the groups they manage.|[Routes API](https://developers.google.com/maps/documentation/routes) \(previously known as Distance Matrix API and Directions API\)|
|Places Autocomplete|Field Service Management utilizes the Places Autocomplete feature to enable type-ahead search behavior in the Google Maps search field.|[Places API \(New\)](https://developers.google.com/maps/documentation/places/web-service/op-overview) \(previously known as Places API\)|

