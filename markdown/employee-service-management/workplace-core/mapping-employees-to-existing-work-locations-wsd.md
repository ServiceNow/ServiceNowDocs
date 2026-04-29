---
title: Mapping employees to their designated workspaces
description: Map your employees to their designated workplace locations in Workplace Core automatically to fill in that detail in reservation requests and to take advantage of auto-assignment of workspaces if that feature has been enabled.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Mapping employees to their designated workspaces

Map your employees to their designated workplace locations in Workplace Core automatically to fill in that detail in reservation requests and to take advantage of auto-assignment of workspaces if that feature has been enabled.

For employees who had a designated workspace before they started working remotely, create a mapping between the user profile and the designated workspace details. This mapping populates the workspace details on reservation request forms so employees don't have to provide these details manually.

If your system administrator has enabled the auto-assign feature, mapping workspaces for all employees also means that designated workspaces are automatically assigned when employees make a reservation request.

The data from the User Workplace Profile \[sn\_wsd\_core\_workplace\_profile\] table is used to automatically assign the designated workspace to the employee.

-   If the user's designated space is available, this space is reserved for the employee.
-   If the designated space is unavailable for the requested date or time, the application searches for and reserves an available space in the employee's workplace in the order of Area &gt; Floor &gt; Building &gt; Campus &gt; Site &gt; Region.

    For example, if no spaces are available in the designated area of the employee, the application finds and reserves an available space from the floor of this area.


**Note:** From Workplace Core version 2.16.1, the workplace user profiles are created in the Workplace Profile Location Assignment \[sn\_wsd\_core\_workplace\_profile\_location\] table. A new field **Is Primary** is added in the table so that you can specify if a location is the primary location when there are multiple locations. In case of existing user profiles created in the User Workplace Profiles \[sn\_wsd\_core\_workplace\_profile\] table, a fix script runs and automatically considers the latest workplace location added to the profile as the primary workplace location.

If you have installed Workplace Space Management application, as a Workplace manager, you can also view the reason for an anomaly in a workplace profile if there are any. A schedule job also enables you to view a detailed report of all the anomalies logged in the application via an email. Navigate to **Workplace Core** &gt; **Administration** &gt; **Workplace profiles** and switch to the Space Management view, a **Reason for anomaly** column appears as a Glide list. An anomaly can happen due to a mismatch in the allocation or assignment type. For more information about anomalies, see [Workplace location assignment anomaly types](../reference/location-assignment-anomaly-types.md).

From Workplace Space Management 1.12.0, only open spaces from the user's allocation type that are within the allocation start and end dates are listed. After an allocation expires, the anomaly is recalculated to the appropriate value.

**Important:** Starting from Workplace Core version 2.16.1, the allocation type **Department and cost center** are no longer available. A new allocation type, **Workplace entity** is introduced that provides more advantages.

-   **[Map designated workspaces to user profiles](../task/map-employees-to-existing-workplace-locations-wsd.md)**  
Map existing designated workspaces to employee user profiles in Workplace Core. This mapping is used to automatically allocate workspaces for employees so they don't have to select a workspace manually when requesting a reservation.
-   **[Set the primary location of a workplace profile](../task/set-prim-location-of-worplace-profile.md)**  
Assign a primary location for the workplace profile if there are multiple locations assigned.

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

[Assign the workplace user role to employees](../task/assign-workplace-user-role-to-employees-of-a-location-wsd.md)

[Configuring shifts for your workplace](configuring-shifts-for-your-workplace-wsd.md)

[Managing workplace shifts that you own](managing-shifts-you-own-wsd.md)

[Managing workplace reservations for employees](managing-workplace-reservations-wsd.md)

[Setting and tracking arrivals at the workplace](scheduling-employees-arrival-to-the-workplace-wsd.md)

[Approve employee workplace reservation requests](../task/approve-workplace-reservation-requests-wsd.md)

[Managing workplace tasks](managing-workplace-maintenance-tasks.md)

[Workplace knowledge management](workplace-knowledge-mgmt-wsd.md)

[QR code management](qr-code-mgmt.md)

[Location migration](location-migration.md)

[View workplace service usage analytics with Usage Insights](../reference/appsee-intergration-wsd.md)

