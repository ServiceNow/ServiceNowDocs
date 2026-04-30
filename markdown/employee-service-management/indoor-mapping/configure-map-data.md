---
title: Configure your map instance data
description: Indoor Mapping provides a set of default parameters to display and configure all your maps.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Indoor Mapping, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Configure your map instance data

Indoor Mapping provides a set of default parameters to display and configure all your maps.

## Before you begin

**Note:** Map editor limited role in the Map Studio has access to only a campus or few assigned campuses. This role can only edit map objects and data for the campuses assigned to it. For more information, see [Configure role-based access in Indoor Mapping](map-limited-editor.md).

To customize and change the map data parameters, update the default parameters in Indoor Mapping. Consider the following before creating your campuses and buildings.

Role required: map editor, map admin

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping**.

2.  Select any of the following map objects to configure and customize the default parameters:

    -   **Campuses**: List of campuses within your organization. Edit to activate or deactivate the campuses.
    -   **Layer types**: Source layers specified in your maps. For example, building, grass, raster, room, wall, etc. Edit the layer types to change names and domains, visible attributes, active and inactive status.
    -   **Place types**: Place types available to display places on the maps. For example, auditorium, bike parking, bus station, etc. Place types are used to display content on the maps. You can edit and modify the names and domains, visible attributes, active and inactive status.
    -   **Direction modes**: Direction modes available for your users. For example, default \(walking\), accessible, bike, etc. You can edit and modify the names and domains, average speed \(used to compute estimated time of arrival\), direction mode icons, active and inactive status.
    -   **Connector types**: Connector types available on your maps. For example, stair, elevator, escalator, ramp, etc. Edit and modify the name and domain, wait time per floor, icon and zoom attributes, active and inactive status.
    -   **Icons**: Icons available on your maps. For example, auditorium, fire extinguisher, computer room, building, etc. Edit and modify the name, title, and domain, active and inactive status, actual file image.
    -   **View types**: View types available on your maps. For example, All, default, minimal. Edit and modify the name, title, and domain, outdoor style, active and inactive status.
    -   **Place groups**: Place groups available on your maps. Edit and modify the name, description, and domain, related campus, active and inactive status.
    -   **Fonts**: Font types available on the map. Edit and modify the name, description, and domain, upload new fonts.
    -   **Outdoor styles**: Outdoor styles available on your maps. For example, default, OpenStreetMap, etc. Edit and modify the name and description, GeoJson description, inactive and active status.

        Default Outdoor navigation styles. Outdoor Style records can be created and modified by map admins \(map\_admin role\). Outdoor style records have a name and a style file. Style files should comply with the Mapbox style specification. For example: `default.json`, `empty.json`, or `openstreetmap.json`.

        The default.json is the default outdoor map style provided and hosted by Indoor Mapping based on OpenStreetMap data and OpenMapTiles. An empty outdoor style has a white background with no outdoor map data at all. The openstreetmap.json has the standard map tiles from OpenStreetMap directly coming from OpenStreetMap.

        **Note:** Users must refer to OpenStreetMap license before using this in production.

    -   Indoor Mapping properties: For more information about how to set the configuration properties, see [Indoor Mapping properties](indoor-mapping-properties.md).

**Parent Topic:**[Configure Indoor Mapping](../concept/configure-ind-mapping.md)

**Previous topic:**[Install Indoor Mapping](install-indoor-mapping.md)

**Next topic:**[Configure role-based access in Indoor Mapping](map-limited-editor.md)

