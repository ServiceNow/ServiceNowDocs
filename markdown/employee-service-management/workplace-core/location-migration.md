---
title: Location migration
description: Learn how to migrate location data from the ServiceNow Locations table to the Workplace Location table to use them in Workplace Service Delivery applications.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Location migration

Learn how to migrate location data from the ServiceNow Locations table to the Workplace Location table to use them in Workplace Service Delivery applications.

You can create a hierarchy to be used while migrating location data from the ServiceNow Location table \[cmn\_location\] to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table.

You can perform the following actions while creating a location migration record:

-   Configure location migration records by setting a parent location and a child location based on which the locations created in the Locations table \[cmn\_location\] are migrated to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table.
-   Specify conditions to filters the locations from the Locations table \[cmn\_location\] based on their Location types.

You can set a location hierarchy configuration as optional depending on the Floor infrastructure. For example, for the **Floor** &gt; **Area** &gt; **Room/Space** hierarchy, you can set the location migration configuration record of **Area** &gt; **Room** as an optional hierarchy because some floors might not have areas or only have spaces or rooms.

When you set a configuration as optional, then the records that do not match that configuration are matched with the next hierarchy. For example, if there are locations that do not match the **Area** &gt; **Room** hierarchy, then they are matched with the next hierarchy, which is **Floor** &gt; **Room**. If there are Rooms that are not assigned to any Areas, then they are matched with Floors because Area is optional.

After migrating the locations, if you create a location in the Workplace Core application, the location is automatically added in the ServiceNow® Location \[cmn\_location\] table. You can configure the type of the location by setting Dictionary Overrides.

-   **[Configure location migration hierarchy](../task/add-location-migration-hierarchy.md)**  
Create a hierarchy for how the location data from the ServiceNow® Location table \[cmn\_location\] must be migrated to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table of Workplace Service Delivery.
-   **[Set the location type in Location table](../task/set-loc-type-in-loc-table.md)**  
Set the location type of a location by creating a dictionary override of the table.

**Parent Topic:**[Manage workplace safety activities](manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet](../task/import-excel-spreadsheet-workspace-data-wsd.md)

[Add a space type configuration](../task/add-space-type-configuration-wsd.md)

[Configure a workplace card](../task/configure-workplace-card.md)

[Block a workplace location](../task/block-workplace-location.md)

[Configure Workplace entity and entity types](workplace-entity.md)

[Managing Neighborhoods](../../workplace-space-management/concept/neighborhoods.md)

[Enable favorites option for Workplace Service Portal](../task/confgure-favourites-option-for-ws-portal-wsd.md)

[Create a workplace performer criteria](../task/create-workplace-performer-criteria.md)

[Mapping employees to their designated workspaces](mapping-employees-to-existing-work-locations-wsd.md)

[Assign the workplace user role to employees](../task/assign-workplace-user-role-to-employees-of-a-location-wsd.md)

[Configuring shifts for your workplace](configuring-shifts-for-your-workplace-wsd.md)

[Managing workplace shifts that you own](managing-shifts-you-own-wsd.md)

[Managing workplace reservations for employees](managing-workplace-reservations-wsd.md)

[Setting and tracking arrivals at the workplace](scheduling-employees-arrival-to-the-workplace-wsd.md)

[Approve employee workplace reservation requests](../task/approve-workplace-reservation-requests-wsd.md)

[Managing workplace tasks](managing-workplace-maintenance-tasks.md)

[Workplace knowledge management](workplace-knowledge-mgmt-wsd.md)

[QR code management](qr-code-mgmt.md)

[View workplace service usage analytics with User Experience Analytics](../reference/appsee-intergration-wsd.md)

