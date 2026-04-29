---
title: The LocationLookup field
description: Any text type can be defined as a LocationLookup component display type, which lets you use Google's API to pull address data.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# The LocationLookup field

Any text type can be defined as a LocationLookup component display type, which lets you use Google's API to pull address data.

The LocationLookup field component display type leverages Googleʼs Places API to pull address data that can be used for unique location configuration and pricing. Any text field type can be defined as a LocationLookup component display type by using the layout editor or by directly editing a layout CSV file.

![CSV file](../images/cpq-location-lookup-csv.png)

To see it in action, view the following video:

[Location Lookup Field Component Display Type](https://www.youtube.com/watch?v=Ofuq7Vza-wU)

To use a LocationLookup field, you first need to have a valid API key from Google with permission to access Google Places. The API key must be configured for both the Maps JavaScript API and the Places API.

The value of the field requires two properties: **key** and **fieldMapping**.

```
{
  "key": API-Key-string,
  "fieldMapping": {"[field1VariableName]":"[returnedPlaceType]","[field2VariableName]":"[returnedPlaceType]"}
}
```

The key property refers to the API key.

Use the fieldMapping property to instruct the UI to map the returned place data to different fields in the configuration. This property can take either a string or an object of key:value pairs \(both strings\).

If a string is provided:

-   The string should be the variable name of a field in the configuration
-   The returned data from the API will be converted to a string and mapped to the field’s value

If an object is provided:

-   The keys will be the variable name of the field in the configuration
-   The values will be the JSON path to the data from the API that should be mapped to the field

For more details on what that data looks like, see: [Place Details](https://developers.google.com/maps/documentation/places/web-service/details#Place)

When you map address components, these come back as an array of the different component values, so there is no straightforward path. The UI expects something in the following format:

```
address_components.[component type]
```

Note that not every type listed is guaranteed to be returned by the place details API. To find the supported types, see the following Google website:

[Place Types](https://developers.google.com/maps/documentation/places/web-service/supported_types)

Example field value:

```
{
    "key": "*********",
    "fieldMapping": {
        "formattedAddress": "formatted_address",
        "sublocality": "address_components.sublocality",
        "city": "address_components.locality",
        "stateForLocation": "address_components.administrative_area_level_1",
        "zipCode": "address_components.postal_code"
    }
}
```

This mapping also works in sets. Note that the location field, and all of the fields listed in the mapping, must also be part of the set. Cross-index or global fields are not supported in a set.

Some common mappings from the Google Places API include:

-   **formatted\_address** \(returns the whole address in human-readable form\)
-   **address\_components.locality** \(returns the city\)
-   **address\_components.administrative\_area\_level\_1** \(returns the state\)
-   **address\_components.country**
-   **address\_components.postal\_code**
-   **address\_components.street\_number**
-   **address\_components.route** \(returns only the street name\)

