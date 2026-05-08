---
title: Map components installed with Indoor Mapping
description: Several types of components are installed with the Indoor Mapping application, including user roles, tables, and scheduled jobs.
locale: en-US
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Reference, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Map components installed with Indoor Mapping

Several types of components are installed with the Indoor Mapping application, including user roles, tables, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

Demo data is available for this plugin.

## Roles installed

<table id="table_kbh_c25_1tb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Indoor Mapping administratorsn\_map\_core.map\_admin

</td><td>

-   Sets up the map data and objects in Indoor Mapping Map Studio.
-   Has complete access to the application.

</td><td>

user\_criteria\_adminCan manage the User Criteria records.

</td></tr><tr><td>

Map editorsn\_map\_core.map\_editor

</td><td>

Sets up maps in the Indoor Mapping Map Studio, imports floor plans, and can manage maps \(edit or delete\) in the Map Studio.

</td><td>

Not applicable.

</td></tr><tr><td>

Map editor limited

sn\_map\_core.map\_editor\_limited

</td><td>

Limits the access to a campus and can only view and edit campuses that are assigned to this role. Users with this role cannot view or update all campuses or map objects in Map Studio.

</td><td>

Not applicable

</td></tr><tr><td>

Map Printer

sn\_map\_core.map\_printer

</td><td>

Allows users to access the map printing page and print maps.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_e4p_yg5_1tb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AutoCAD Source\[sn\_map\_core\_autocad\_source\]

</td><td>

Provides the needed data and the user setup for an Autocad file to generate \(import\) places and layers.

</td></tr><tr><td>

Autocad source block\[sn\_map\_core\_autocad\_source\_block\]

</td><td>

Automatically generated after an Autocad file upload, provides the data needed to extract autocad blocks into map places.

</td></tr><tr><td>

Autocad source layer\[sn\_map\_core\_autocad\_source\_layer\]

</td><td>

Automatically generated after an Autocad file upload, provides the data needed to extract autocad layers into map layers.

</td></tr><tr><td>

Autocad source text\[sn\_map\_core\_autocad\_source\_text\]

</td><td>

Automatically generated after an autocad file upload, provides the data needed to extract autocad texts into map places.

</td></tr><tr><td>

Campus\[sn\_map\_core\_campus\]

</td><td>

Provides the campus name, address and geometry. A campus contains a set of buildings.

</td></tr><tr><td>

Building\[sn\_map\_core\_building\]

</td><td>

Provides the building name, campus, address and geometry. A building contains a set of floors.

</td></tr><tr><td>

Floor\[sn\_map\_core\_floor\]

</td><td>

Provides the floor name and number. A floor contains a set of places.

</td></tr><tr><td>

Font\[sn\_map\_core\_floor\]

</td><td>

Manage fonts for indoor maps.

</td></tr><tr><td>

Connector\[sn\_map\_core\_connector\]

</td><td>

Manage connector and connector types to a building like stairs, escalators, elevators, and stairs.

</td></tr><tr><td>

Connector Type\[sn\_map\_core\_connector\_type \]

</td><td>

Organizes connectors into types to provide a common style and information like waiting time and the direction of the connectors, for example: elevator.

</td></tr><tr><td>

Direction Modesn\_map\_core\_direction\_mode

</td><td>

Defines the route preferences, for example: accessible.

</td></tr><tr><td>

Icon\[sn\_map\_core\_icon\]

</td><td>

Provides an icon to be used on the map for places, buildings, campuses, connectors and direction modes.

</td></tr><tr><td>

Tile\[sn\_map\_core\_tile \]

</td><td>

Automatically generated after a raster\_source is imported, provides the location and image for the tiles generated for the imported layer.

</td></tr><tr><td>

Job\[sn\_map\_core\_job\]

</td><td>

Manage jobs.

</td></tr><tr><td>

View content\[sn\_map\_core\_view\_content \]

</td><td>

Provides a style and content for a campus displayed in a view type. The style can be provided for the campus, building, place, connector, layer, place type, connector type and layer type.

</td></tr><tr><td>

Layer\[sn\_map\_core\_layer\]

</td><td>

Manage floor plan layer.

</td></tr><tr><td>

Layer type\[sn\_map\_core\_layer\_type\]

</td><td>

Organizes layers into types to provide a common style.

</td></tr><tr><td>

Place\[sn\_map\_core\_place \]

</td><td>

Provides the place name and geometry.

</td></tr><tr><td>

Place type\[sn\_map\_core\_place\_type\]

</td><td>

Organizes places into types to provide a common style.

</td></tr><tr><td>

View type\[sn\_map\_core\_view\_type \]

</td><td>

Provides multiple styles for the same campus. It can also be used to display a different content for the same campus.

</td></tr><tr><td>

Entrance\[\]sn\_map\_core\_place\_entrance

</td><td>

Provides the locations of the place entry.

</td></tr><tr><td>

Place Marker\[sn\_map\_core\_place\_marker\]

</td><td>

Provides the locations of the place marker

</td></tr><tr><td>

Node\[sn\_map\_core\_node\]

</td><td>

Provides the location of a node in the direction graph.

</td></tr><tr><td>

Routes\[sn\_map\_core\_route \]

</td><td>

Provides a path between two nodes.

</td></tr><tr><td>

Raster source\[sn\_map\_core\_raster\_source \]

</td><td>

Provides the needed data and the user setup to generate \(import\) an image layer.

</td></tr><tr><td>

Campus editorsn\_map\_core\_m2m\_campus\_editor

</td><td>

Enables users to edit a campus using user criteria.

</td></tr><tr><td>

Connector to direction mode associations\[sn\_map\_core\_m2m\_connector\_direction\_mode\]

</td><td>

Manage connectors and direction modes on a building.

</td></tr><tr><td>

Route to direction mode associations\[sn\_map\_core\_m2m\_route\_direction\_mode\]

</td><td>

Maps routes with relevant direction modes.

</td></tr><tr><td>

View type and Campus to direction mode associations\[sn\_map\_core\_m2m\_view\_type\_campus\_direction\_mode\]

</td><td>

Allows a direction mode to be used inside a campus displayed with a view type.

</td></tr><tr><td>

View type reader\[sn\_map\_core\_m2m\_view\_type\_reader \]

</td><td>

Allows a users to display a view type using a user criteria.

</td></tr><tr><td>

View type and campus to user criteria associations\[sn\_map\_core\_m2m\_view\_type\_campus\_reader\]

</td><td>

Allows users to display a campus with a view type using a user criteria.

</td></tr><tr><td>

Font\[sn\_map\_core\_font \]

</td><td>

Required fonts for outdoor styles.

</td></tr><tr><td>

Outdoor style\[sn\_map\_core\_outdoor\_style \]

</td><td>

Defines the style of the street map displayed behind the indoor map.

</td></tr><tr><td>

Snapshotsn\_map\_core\_snapshot

</td><td>

Creates snapshot to migrate data across instances.

</td></tr><tr><td>

Place properties mappingsn\_map\_core\_place\_properties

</td><td>

Extracts room dimensions from a CAD source file.

</td></tr><tr><td>

CAD Configuration item\[sn\_map\_core\_cad\_configuration\_item\]

</td><td>

Internally used by the Map Studio to save configuration made for an Autocad source.

</td></tr><tr><td>

CAD Diffsn\_map\_core\_cad\_diff

</td><td>

Internally used by Map Studio to save the changes made to an Autocad source in the CAD Editor.

</td></tr><tr><td>

Indoor Map / WSD Synchronization\[sn\_wsd\_indoor\_map\_sync\]

</td><td>

Synchronizes Indoor Mapping map data with Workplace Service Delivery data.

</td></tr><tr><td>

Indoor Map / WSD Buildings Synchronization\[sn\_wsd\_indoor\_map\_building\_sync\]

</td><td>

Synchronizes Indoor Mapping building data with Workplace Core building data.

</td></tr><tr><td>

Indoor Map / WSD Cleaning\[sn\_wsd\_indoor\_map\_clean\_sync\]

</td><td>

Table used by the synchronization process between Indoor Mapping and Workplace Service Delivery. Cleaning step is a part of the synchronization process.

</td></tr><tr><td>

Indoor Map / WSD Floors Synchronization\[sn\_wsd\_indoor\_map\_floor\_sync\]

</td><td>

Synchronizes Indoor Mapping floor data with Workplace Core floor data.

</td></tr><tr><td>

Indoor Place Properties Mapping\[sn\_wsd\_indoor\_map\_place\_properties\_mapping\]

</td><td>

Indoor Mapping properties.

</td></tr><tr><td>

Indoor Map / WSD Spaces Synchronization\[sn\_wsd\_indoor\_map\_space\_sync\]

</td><td>

Synchronizes Indoor Mapping spaces data with Workplace Core space data.

</td></tr><tr><td>

Indoor Map / WSD Types Synchronization\[sn\_wsd\_indoor\_map\_type\_sync\]

</td><td>

Synchronizes Indoor Mapping place types data with Workplace Core space types data.

</td></tr><tr><td>

Indoor Map / CMN Location Buildings Synchronization\[sn\_map\_core\_building\_sync\]

</td><td>

Synchronizes Indoor Mapping building data with CMN location buildings data.

</td></tr><tr><td>

Source\[sn\_map\_core\_source\]

</td><td>

Parent table for all kind of sources in Indoor Mapping. Sources are files \(raster or PNG files or CAD files \) that can be imported to create floor plans.

</td></tr><tr><td>

Autocad source\[sn\_map\_core\_autocad\_source\]

</td><td>

Stores Autocad file and data about the file.

</td></tr><tr><td>

Autocad source block\[sn\_map\_core\_autocad\_source\_block\]

</td><td>

Internally used by Map Studio. Stores information about block references present in an Autocad file.

</td></tr><tr><td>

Autocad source layer\[sn\_map\_core\_autocad\_source\_layer\]

</td><td>

Internally used by Map Studio. Stores information about layer configuration present in an Autocad file.

</td></tr><tr><td>

Autocad source text\[sn\_map\_core\_autocad\_source\_text\]

</td><td>

Internally used by Map Studio. Stores information about text present in an Autocad file.

</td></tr><tr><td>

Print Request\[sn\_map\_core\_print\_request\]

</td><td>

Internally used by the Indoor Mapping application. Stores information about print requests that are raised by users.

</td></tr></tbody>
</table>## Scheduled jobs

<table id="table_i2d_5mn_htb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clean old Indoor Mapping tiles \(old versions &gt; 3 days\)

</td><td>

A schedule job is running every days to purge data that are not relevant anymore in the tiles table. The tiles tables stores data generated from PNG file import process.

 When a new PNG is upload to retrieve an existing one, previous generated tiles are not used anymore and therefore, will be purge by the scheduled job.

</td></tr><tr><td>

Sync script Notification

</td><td>

A notification is sent to the administrator if changes were made to Indoor Mapping map data objects and the synchronization script is not run. The notification reminds the administrator that the data might not be in synchronized and that the synchronization process must be run.

</td></tr></tbody>
</table>**Parent Topic:**[Indoor Mapping references](../concept/indoor-mapping-references.md)

**Previous topic:**[Indoor Mapping references](../concept/indoor-mapping-references.md)

**Next topic:**[Indoor Mapping terminology](indoor-mapping-common-terminology.md)

