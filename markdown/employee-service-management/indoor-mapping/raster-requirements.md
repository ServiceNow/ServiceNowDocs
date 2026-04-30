---
title: Raster file requirements
description: Raster files are flat files and therefore, design and places have to be manually created. Raster floor plan files must meet the Map Studio import requirements.
locale: en-US
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Raster file requirements

Raster files are flat files and therefore, design and places have to be manually created. Raster floor plan files must meet the Map Studio import requirements.

If you are importing a raster image \(PNG\) source, the designs and place creation process must be performed manually in a graphic designer tool. For example: Adobe Illustrator. Currently, only PNG file formats are supported.

**Note:** Map administrators must ensure that the floor plan sources adhere to the import requirements of Indoor Mapping. Before importing, ensure that the raster image \(PNG\) sources are reviewed by graphic designers for design corrections and accuracy. Import of JSON/GEOJSON files is only available for third-party mapping providers migration.

For more information about raster file import requirements, see [ServiceNow Blog](https://www.servicenow.com/community/wsd-blog/png-guidelines-for-indoor-mapping/ba-p/2266959?attachment-id=209840).

<table id="table_jvv_p4t_1tb"><thead><tr><th>

Design properties

</th><th>

Requirements

</th></tr></thead><tbody><tr><td>

Floor plan proportions

</td><td>

-   Ensure that your design studio Artboard has 20,000 x 20,000 pixels ratio for optimal image rendering.
-   Ensure that the floor plan occupies the complete Artboard in your design studio. Image quality is based on the Artboard size. If the floor plan does not fit the whole Artboard, then, the final size is reduced and may get pixelated.
-   Verify that the building is at scale to match the real building proportion and shape on the outdoor map. If the building proportions are not accurate, time, and distances for directions are not accurate.

</td></tr><tr><td>

Design

</td><td>

-   Redesign your floor plan for ease of use. Floor plans must be as simple as possible so that end users can easily understand the map.

-   Ensure that all text objects are removed from the raster image file. Text objects are not supported on the PNG file for floor plans.

**Note:** Places for spaces are added to describe places on a map. Therefore, text objects on a map can be confusing to end users.

-   Remove the image borders. All the spaces around a building must be removed or made transparent.

</td></tr><tr><td>

Export

</td><td>

Export the image file with the following requirements:-   Type: Currently, only PNG and JPEG raster image sources are supported in Indoor Mapping.
-   Size: Image file must not exceed 50 MB.
-   Dimensions: Image dimension must be 20,000 x 20,000 pixels.

</td></tr></tbody>
</table>1.  [Import Raster files](../task/import-raster-files.md)  
After creating your campus, buildings, and floor, upload and import the raster floor plan sources.

**Parent Topic:**[Indoor Mapping](../reference/Indoor-mapping.md)

