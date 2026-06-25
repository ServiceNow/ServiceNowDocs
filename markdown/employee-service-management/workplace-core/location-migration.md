---
title: Location migration
description: Learn how to migrate location data from the ServiceNow Locations table to the Workplace Location table to use them in Workplace Service Delivery applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/location-migration.html
release: australia
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Location migration

Learn how to migrate location data from the ServiceNow Locations table to the Workplace Location table to use them in Workplace Service Delivery applications.

You can create a hierarchy to be used while migrating location data from the ServiceNow Location table \[cmn\_location\] to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table.

You can perform the following actions while creating a location migration record:

-   Configure location migration records by setting a parent location and a child location based on which the locations created in the Locations table \[cmn\_location\] are migrated to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table.
-   Specify conditions to filter the locations from the Locations table \[cmn\_location\] based on their Location types.

You can set a location hierarchy configuration as optional depending on the Floor infrastructure. For example, for the **Floor** &gt; **Area** &gt; **Room/Space** hierarchy, you can set the location migration configuration record of **Area** &gt; **Room** as an optional hierarchy because some floors might not have areas or only have spaces or rooms.

When you set a configuration as optional, then the records that don’t match that configuration are matched with the next hierarchy. For example, if there are locations that don’t match the **Area** &gt; **Room** hierarchy, then they’re matched with the next hierarchy, which is **Floor** &gt; **Room**. If there are Rooms that aren’t assigned to any Areas, then they’re matched with Floors because the Area is optional.

After migrating the locations, if you create a location in the Workplace Core application, the location is automatically added in the ServiceNow® Location \[cmn\_location\] table. You can configure the type of the location by setting Dictionary Overrides.

-   **[Configure location migration hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/add-location-migration-hierarchy.md)**  
Create a hierarchy for how the location data from the ServiceNow® Location table \[cmn\_location\] must be migrated to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table of Workplace Service Delivery.
-   **[Set the location type in Location table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/set-loc-type-in-loc-table.md)**  
Set the location type of a location by creating a dictionary override of the table.

**Parent Topic:**[Manage workplace safety activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet]()

[Add a space type configuration]()

[Configure a workplace card]()

[Block a workplace location]()

[Configure Workplace entity and entity types]()

[Managing Neighborhoods]()

[Enable favorites option for Workplace Service Portal]()

[Create a workplace performer criteria]()

[Mapping employees to their designated workspaces]()

[Assign the workplace user role to employees]()

[Configuring shifts for your workplace]()

[Managing workplace shifts that you own]()

[Managing workplace reservations for employees]()

[Setting and tracking arrivals at the workplace]()

[Approve employee workplace reservation requests]()

[Managing workplace tasks]()

[Workplace knowledge management]()

[QR code management]()

[View workplace service usage analytics with Usage Insights]()

