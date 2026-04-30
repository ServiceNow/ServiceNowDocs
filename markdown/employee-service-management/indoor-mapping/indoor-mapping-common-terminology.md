---
title: Indoor Mapping terminology
description: Key terms used in Indoor Mapping.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reference, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Indoor Mapping terminology

Key terms used in Indoor Mapping.

<table id="table_dxg_jqf_1tb"><thead><tr><th>

Terms

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Blocks

</td><td>

Blocks are an Autocad feature which groups text element of a CAD file together to create blocks for desks, meeting rooms, etc.

</td></tr><tr><td>

Boundary

</td><td>

Represents the limit of a campus or building.

</td></tr><tr><td>

Building

</td><td>

Represents a physical building. A campus may contain multiple buildings. A building can have multiple floors.**Note:** A building must belong to a campus.

</td></tr><tr><td>

Campus

</td><td>

A campus contains a set of buildings and outdoor elements like:-   Places that represent outdoor points or place types. For example: bus stop, fire hydrant, visitor gate, and so on.
-   Layers representing outside elements in buildings. For example: walking paths, trees, park, and so on.
-   Nodes and routes to represent possible directions in buildings.

</td></tr><tr><td>

Campus \(Outdoor\)

</td><td>

Campus \(outdoor\) are the graphic elements \(e.g. trees or logos\) or Places \(e.g. bus stop, restaurant\) placed on the world map. Outdoor elements do not depend on a building floor and are displayed.

</td></tr><tr><td>

Connectors

</td><td>

Defines the physical means to change floors \(e.g. stairs, escalators, ramps or elevators\). Connectors are added on the direction graph nodes.

</td></tr><tr><td>

Connector types

</td><td>

Defines the kind of connectors available in an instance \(e.g. ramps, escalators, elevators, etc.\). A connector type contains the style \(icon\) and properties for each connector. New connector types can be created at the instance level.

</td></tr><tr><td>

Directions or Direction graph

</td><td>

Represents a set of connected lines and nodes created in Map Studio to provide Wayfinding on the map.

</td></tr><tr><td>

Direction Modes

</td><td>

Defines multiple modes of directions or means of transportation \(for example Pedestrian, Accessible, Bike, Truck etc.\). Extra modes can be created at the instance level.

</td></tr><tr><td>

Entrance \(Polygons\)

</td><td>

Polygon entrances define where the door of a space is located so that the wayfinding engine enters the room accordingly.

</td></tr><tr><td>

Floor

</td><td>

Represents a floor of a particular building.

</td></tr><tr><td>

Floor plan sources

</td><td>

Defines the original data source or file to import in Map Studio in order to create an Indoor Map. It can either be a PNG or DWG/DXF.

</td></tr><tr><td>

Floor controller

</td><td>

Represents a list of floors or buttons to click on to visualize the different building levels.

</td></tr><tr><td>

Georeference

</td><td>

Action of positioning a floor plan at its exact location on the world map.

</td></tr><tr><td>

Indoor mapping application

</td><td>

The Indoor Mapping application is the plugin that must be installed in order to have Map Studio and configure an Indoor Map.

</td></tr><tr><td>

IPS

</td><td>

Indoor Positioning System also known as the technology providing the blue dot on the map.

</td></tr><tr><td>

Layers

</td><td>

Layers are part of the CAD file and represent the elements of a floor plan \(e.g. Pipes, rooms, columns, etc.\)

</td></tr><tr><td>

Layer Type

</td><td>

Defines type of layers like walls, columns, heating pipes, and so on. They are defined at the instance level. They are used to categorize the imported elements and to style them \(CAD import only\).

</td></tr><tr><td>

Map Studio

</td><td>

Map Studio is the tool to create, edit and maintain Indoor Maps.

</td></tr><tr><td>

Marker

</td><td>

A marker is a pin placed on a campus/building/polygon to display the icon and the title.

</td></tr><tr><td>

Name

</td><td>

The name is an admin ID for an imported or created element \(e.g. name of a place\).

</td></tr><tr><td>

Nodes

</td><td>

Defines points along the direction graph. Nodes are also used to create connectors to change floor.

</td></tr><tr><td>

Outdoor style

</td><td>

Represents the “outside” in between buildings \(default, open street map, etc\). New outdoor styles can be created at the instance level.

</td></tr><tr><td>

Places

</td><td>

Places refer to any element placed on the map that users will be able to search for. It can be a meeting room, library, park etc. Places are either polygons or points. They can be automatically imported from a CAD file or manually created on Map Studio.

</td></tr><tr><td>

Place Types

</td><td>

Place Types are added to points of interest to categorize and style them with the right icon and color. New Place. Types can be created at the instance level.

</td></tr><tr><td>

Polygon \(places\)

</td><td>

A polygon is made of a pin and a shape. Polygons are mandatory for meeting rooms to have a shape to color green or red according to the booking status.

</td></tr><tr><td>

Point \(places\)

</td><td>

A point is a pin placed on the map that does not have a shape around it.

</td></tr><tr><td>

Raster image file

</td><td>

Supports import of raster PNG image for main floor plan. The raster image provides one raster tile layer for a floor.

</td></tr><tr><td>

Segment or Route

</td><td>

Defines a line between two nodes.

</td></tr><tr><td>

Style editor

</td><td>

To create, configure and style a view.

</td></tr><tr><td>

Text

</td><td>

Text is an AutoCAD feature used to add text elements on a CAD layer. That way, users can create Text elements for desks, meeting rooms and so on.

</td></tr><tr><td>

Tile

</td><td>

The title is what will be displayed on the map to end users \(e.g. title of a place\).

</td></tr><tr><td>

View

</td><td>

A view is composed of content and style that will be displayed for certain users. Views are configured in the style editor. For example, admins can create an Employee view type and go to the style editor to decide what they want to display in that view. They can also select the style of these elements for that view.

</td></tr><tr><td>

View types

</td><td>

Provides a name to a specific view \(e.g. Employee, maintenance, etc.\). View types can be created at the instance level.

</td></tr><tr><td>

Wayfinding

</td><td>

Automated algorithm displaying a path between an origin and a destination. Wayfinding is different from Indoor Positioning and doesn’t contain a blue dot.

</td></tr><tr><td>

Zoom Level / Default Zoom

</td><td>

Defines at which Zoom levels certain elements will be displayed or at which Zoom level a campus will open.

</td></tr></tbody>
</table>**Parent Topic:**[Indoor Mapping references](../concept/indoor-mapping-references.md)

**Previous topic:**[Map components installed with Indoor Mapping](components-installed-with-indoor-mapping.md)

**Next topic:**[Snapshot Impacted tables](snapshot-ind-mapping-tables.md)

