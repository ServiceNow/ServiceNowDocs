---
title: Autocad import requirements
description: After adding a building, you can start importing your CAD floor plan source file in the Map Studio.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: concept
last_updated: "2025-02-06"
reading_time_minutes: 2
breadcrumb: [Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Autocad import requirements

After adding a building, you can start importing your CAD floor plan source file in the Map Studio.

Creating indoor maps in Indoor Mapping can be done by manually importing the CAD floor plan sources or by automating the import process using the AutoCAD import capability in the Map Studio. CAD files must meet certain requirements in the Map Studio before the CAD source files are imported. For more information, see [ServiceNow Blog](https://www.servicenow.com/community/wsd-blog/cad-file-guidelines-for-indoor-mapping/ba-p/2266775)

**Note:** Map administrators must ensure that their CAD sources adhere to the import requirements of Indoor Mapping Map Studio. Before importing, ensure that the AutoCAD sources are reviewed by graphic designers for design corrections and accuracy. Import of JSON or GEOJSON files is only available for third-party mapping provider migration process.

AutoCAD files up to 200 MiB can be uploaded to the Map Studio. Uploading larger files can result in performance degradation.

Please note that even if the file is below 200MiB, the generated data might be higher depending on the file features, and this can also result in performance degradation or import issues.

## File

Floors in a building should reside on an isolated file. Indoor Mapping Map Studio can only read and load one floor per file. Hence, it is important that each floor is on a unique file.

## Layers

All building layers must be separated. Floor plans in AutoCAD are created using a layer system. It is important that each building element is on a different layer to style or delete elements. Display only layers that your map users need. Make sure you don’t have any unnecessary details on your file as layers with too many elements can block the import process.

**Note:** Interactive maps must be as clear as possible. Remove non-essential items such as sinks or windows. Sort the elements when importing your floor plan by placing these elements on a separate layer.

All text objects must be isolated on a dedicated layer according to their type. Each type of object must have its own text layer.

Drawings must be isolated on a dedicated layers based on the drawing type. Ensure that each room type is on a separate layer. If you are merging elements, ensure that they imported with the same line and background color.

Names must be clear and identical from one file to another. On Map Studio, after a file is imported, the configuration is retained and automatically applied to other files only if the layer names are identical \(available only in Tokyo and later releases\). Map admins, map creators or map editors cannot recognize the different layers in the Map Studio if your files have different layer names. The CAD configurations are not performed automatically.

## Lines

All lines must be connected to form closed shapes. Lines in the CAD file are used to draw the floor plan and define your building outline, rooms and inaccessible areas. Spaces outside the closed lines are considered open areas. For example, hallways.

Ensure that all lines and shapes are properly closed. For example, if shapes are not properly closed, rooms in a hallway are not considered a part of a hallway and points are created in the rooms.

## Export

Export your CAD file in DWG or DXF formats. Other formats are not supported. Make sure you are exporting the right version of CAD file. AutoCAD 12 \(AC1009\) to AutoCAD 2018–2021\(AC1032\) is supported in Indoor Mapping Map Studio.

**Parent Topic:**[Manage CAD source files](manage-autocad-files.md)

