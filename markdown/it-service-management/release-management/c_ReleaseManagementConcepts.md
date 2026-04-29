---
title: Release Management concepts
description: The Release Management application encompasses the planning, design, build, configuration, and testing of hardware and software releases to create a defined set of release components.
locale: en-US
release: australia
product: Release Management
classification: release-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Release Management, IT Service Management]
---

# Release Management concepts

The Release Management application encompasses the planning, design, build, configuration, and testing of hardware and software releases to create a defined set of release components.

Release management comprises of a series of activities performed to ensure that the changes are applied successfully to both pre-production and product environments.

![Release Management](../image/rm-concepts.png)

|Concept|Description|
|-------|-----------|
|Products|Represents the hardware or software for which releases are built. A product can be linked with a Business Service in the CMDB to link it with other ITIL processes.|
|Releases|Bundles all the work done \(projects, epics, stories, enhancements, defects, problems, incidents, and so on\) for products or services together and ensures that these work items are built, tested, and deployed on non-production and/or production environments.|
|Release Phases|Represents the planned phases within a release, which are used to group the tasks required to carry out the release. For example, gathering requirements, planning, design, development, testing, and deployment.|
|Release Tasks|Represents any of the tasks required to implement a feature of a product.|

![Table relationships](../image/table-relationships.png "Table relationships in Release Management")

**Note:** The tables for Feature and Feature Task under a release are not removed. If you already use Feature and Feature Task under a release, you can continue doing so.

-   **[Default state categories for Release and Release task tables](../reference/default-state-categories-for-release-and-release-task-tables.md)**  
Understand how the different states of the Release \[rm\_release\] and Release Task \[rm\_task\] tables are configured by default. Use this information to customize the states according to your organizational release processes.

**Parent Topic:**[Release Management](c_ITILReleaseManagement.md)

