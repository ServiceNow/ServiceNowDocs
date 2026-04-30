---
title: Space management
description: The concept of space is part of the Facilities Service Management application. Space provides a definition at all levels with the same unit measure, and presents metrics that are readily available for analysis. These metrics include occupancy percentage, total space available, and so on.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Space management

The concept of space is part of the Facilities Service Management application. Space provides a definition at all levels with the same unit measure, and presents metrics that are readily available for analysis. These metrics include occupancy percentage, total space available, and so on.

**Note:** This feature is no longer available for new customers.

The additional benefits of space management include:

-   Ability to forecast future space requirements
-   Simplification of the charge back process
-   Space analysis for actual and planned use cases
-   Addition of zones for creating different collections of spaces

## Space hierarchy

A natural hierarchy models all the spaces of your organization. You can use this information to determine how effectively you are using your facilities space. The hierarchy from top to bottom is campus, building, level \(floor\), and space.

You can create types of spaces as needed. New space definition tables extend the \[fm\_space\] table. Be sure to set the proper ACLs. The following graphic depicts how tables are related to one another.

![Picture depicts order of tables as fm_campus, alm_building, fm_level, and fm_space and how they are extended](../image/SpaceHierarchy.png "Space table hierarchy")

## Space roll up calculations

The Facilities Service Management application can roll up occupancy, area, and usage information from lower to higher levels in the space hierarchy. Roll ups are spaces designated as available for occupancy. The occupancy values from that space roll up to the level above them.

When you designate a space as available for occupancy, you can also specify the maximum occupancy. Depending on the actual occupancy, a percentage appears to show how much space is available. A script include modifies the roll-up calculations.

![image is a screenshot showing the available occupancy check box and dependant fields](../image/Occupiable.png "Available for occupancy selected and dependent fields")

The values that roll up are:

-   Occupancy
-   Max occupancy
-   Assignable area

The percent occupied calculation takes place based on the current and max occupancy values.

## Associated users

You can assign users to more than one location, with a primary location.

Assign employees a primary location. A business rule ensures that an employee can have only one primary location. Employees that travel between campuses can have an assigned space on each campus. The \[fm\_m2m\_user\_to\_space\] table stores these records. Adding a user automatically updates the current occupancy and availability status of the space and performs the percent occupied calculation.

**Note:** Space becomes available when a user becomes inactive.

## Associated departments

You can assign spaces to more than one department for cost allocation and reporting purposes.

The Associated Department \[fm\_m2m\_department\_to\_space\] table extends the fm\_space table, containing the relationship of departments and percentage ownership. A percentage automatically calculates after setting the weight for each department. A business rule sets the percentages based on weight so that the sum of percentages equals 100%.

-   **[GeoJSON map files](r_GeoJSONMapFiles.md)**  
The floor plan visualization feature uses files in the GeoJSON format, an open standard for representing geographical features.
-   **[Customer-created maps](r_Manually-builtMaps.md)**  
Creating a map begins with the addition of the campus, then the buildings, floors, and other spaces.
-   **[Run transform to update data](../task/t_RunTransform.md)**  
Running a transform exports information from your records into an .xls file. That data can be imported into the ServiceNow space management application.

**Parent Topic:**[Facilities Service Management overview](../concept/c_FacilitiesServiceManagement.md)

