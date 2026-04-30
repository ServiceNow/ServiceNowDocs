---
title: GeoJSON map files
description: The floor plan visualization feature uses files in the GeoJSON format, an open standard for representing geographical features.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# GeoJSON map files

The floor plan visualization feature uses files in the GeoJSON format, an open standard for representing geographical features.

Due to the complexity of each file, work with Micello, Inc. or some other vendor to create the floor plan for your organization.

**Note:** However, creating a floor plan requires GeoJSON knowledge. Ensure that you are familiar with geospatial data and/or GeoJSON data before attempting this task.

For information about the GeoJSON standard, see [http://geojson.org](http://geojson.org). Object properties in the GeoJSON files are used to create buildings, floors, and spaces.

When cloning an instance, sys\_attachments including GeoJSON maps are not cloned by default. See the **Exclude large attachment data field** in [Request a clone](https://www.servicenow.com/docs/access?context=t_StartAClone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) .

**Note:** As an option, you can download the GeoJSON maps from the source tables \(fm\_map\_set and fm\_map\_set\_tranformed\) and upload to the destination.

-   **[Community file](r_CommunityFile.md)**  
The community file contains information about the campus, including the number of buildings and the number of floors for each building.
-   **[Level geometry file](r_LevelFile.md)**  
The level geometry file contains all the geometry for a given level. Each file is one map that can be rendered in the ServiceNow platform.
-   **[Process GeoJSON map files](../task/t_ProcessMapFiles.md)**  
Processing GeoJSON map files includes parsing data from a map and importing that information to the campus space management tables. Use this process to set up your spaces or update bulk changes to your campus without having to enter each change manually.

**Parent Topic:**[Space management](r_SpaceManagement.md)

