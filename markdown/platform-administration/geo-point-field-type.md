---
title: Geo point field type
description: The geo point data type stores longitude and latitude coordinates.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Geo point field type

The geo point data type stores longitude and latitude coordinates.

You can store longitude and latitude coordinates by adding a geo point data type field to any table. For example, you can define a geo point field to store a longitude and latitude pair to help technicians find the location of a part in a warehouse.

Function fields provide several glidefunction operations for working with geo point fields.

-   Calculate the distance between geo points using distance\_sphere\(\) in a function field and use it to order records in a list based on how far away the warehouse is. For example:

    ```
    glidefunction:distance_sphere(geopointField1, geopointField2)
    ```

-   Convert longitude and latitude columns to a geo point field using get\_longitude\(\) and get\_latitude\(\) in a function field. For example:

    ```
    glidefunction:get_latitude(u_geo_point_field)
    ```

    ```
    glidefunction:get_longitude(u_geo_point_field)
    ```

-   Convert a geo point field or any valid numeric values or columns into longitude and latitude columns or values using to\_geopoint\(\) in a function field. For example:

    ```
    glidefunction:to_geopoint(u_long_column, u_lat_column)
    ```


See [Function field](../../../build/platform-functions/concept/platform-support-functions.md#).

Values for geo points are in longitude, latitude format where:

-   Both longitude and latitude are restricted to 6 decimal places of precision. For example, “80.206458”, “25.767242”.
-   The longitude range is \[-180, 180\].
-   The latitude range is \[-90, 90\].
-   Values entered outside the ranges for longitude or latitude are normalized to values inside their respective ranges.

