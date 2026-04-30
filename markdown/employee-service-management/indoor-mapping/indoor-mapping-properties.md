---
title: Indoor Mapping properties
description: Customize and render map components and objects by updating the Indoor Mapping properties.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Indoor Mapping properties

Customize and render map components and objects by updating the Indoor Mapping properties.

## Before you begin

Role required: map admin, map editor

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Indoor Mapping Properties**.

    Indoor Mapping properties are displayed. Customize the map component properties as required.

2.  Fill in the form fields.

<table id="table_uqn_z5c_nwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Map import service URL

</td><td>

Option to define the URL from where the Map Import Service can be reached to enable floor plans. This property is mapped to the **\(sn\_map\_core.map\_import\_service.url\)** system property.

</td></tr><tr><td>

Default outdoor style used in the Map Studio

</td><td>

Specifies the default outdoor style used in the Map Studio. This property uses the outdoor style table record including the default ones and customized styles. This property is mapped to the **sn\_map\_core.studio.default\_outdoor\_style**system property.

 **Note:** Do not use the “Empty” outdoor style as you cannot georeference floor plans with it.

</td></tr><tr><td>

Decide whether or not the system should prevent studio to make a call to Google geocoding API.

</td><td>

Mapped to the **sn\_map\_core.studio.prevent\_google\_geocoding** system property. This option if selected helps to prevent the Map Studio from making a call to Google geocoding API. The Google geocoding API is used by default in the Map Studio to provide suggestions for location address and center the map on the selected location address while creating a campus. You can prevent the use of the Google geocoding API while creating a campus by zooming into the world map to point to the location of the campus.

</td></tr><tr><td>

Maximum number of user criteria considered to determine campus editors.

</td><td>

Maximum number of users that can be campus editors. This property can be increased if the number of users as campus editors is more than 100. This may impact the Map Studio performance. Default value is 100 and is mapped to the **sn\_map\_core.max\_user\_criteria\_count** system property.

</td></tr><tr><td>

Maximum distance in centimeters between the first and last point to convert a line to a polygon while importing an AutoCAD file \[sn\_map\_core.line\_to\_polygon\_max\_distance

\]

</td><td>

Option to automatically close all lines that are one centimeter apart on a CAD file. Creating a polygon on the map requires the poly lines to be closed in a CAD file before you import the CAD file in the Map Studio. When the lines are not closed, enabling this property helps to deduct and close the open lines in a polygon.

</td></tr><tr><td>

Set to true to ignore hidden CAD layers during imports

</td><td>

Option to ignore any hidden CAD layers present in the AutoCAD source file. When this option is enabled, the hidden CAD layers are not shown on the map.

</td></tr><tr><td>

Comma-separated list of CAD layers to ignore during imports \(e.g. layer1,layer2\)

</td><td>

Option to ignore the CAD layers that you do not want to display or show on the map. The layers even if not hidden are ignored. Provide the names of layers that you want to ignore as a comma-separated list. The ignored layers are not displayed on the map after you import the CAD file.

</td></tr><tr><td>

Set to true to enable the simplification of GeoJSON features during CAD imports

</td><td>

Option to reduce the complexity of geometries extracted from the CAD file to improve performance using the **sn\_map\_core.cad\_simplify\_enabled** system property.

</td></tr><tr><td>

Tolerance of the simplification algorithm that can be run during AutoCAD imports if all conditions are met

</td><td>

Option to change the accuracy of the simplification algorithm by using use the system property **sn\_map\_core.cad\_simplify\_tolerance**. It is set to 0.1 by default which defines the level of simplification where '0' is the original geometry and nothing is changed in the geometry. When this option is set to 0.1, it provides the most accurate results by simplifying the geometry. For example, if you increase the value to 0.8, then a circle may become a triangle and the accuracy of geometry is reduced as it removes the coordinates on a geometry.

</td></tr><tr><td>

Minimum number of coordinates in a GeoJSON feature to run the simplification algorithm \(if enabled\) during AutoCAD imports.

</td><td>

Threshold to simplify complex shapes or geometries that have 20 or more coordinates by using the **sn\_map\_core.cad\_simplify\_coords\_cnt\_threshold** property. Default value is 20 coordinates. After uploading the CAD file in the Map Studio, import it to see the reduced coordinates or points on the map.

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Configure Indoor Mapping](../concept/configure-ind-mapping.md)

**Previous topic:**[Configure role-based access in Indoor Mapping](map-limited-editor.md)

**Next topic:**[Manage CAD source files](../concept/manage-autocad-files.md)

