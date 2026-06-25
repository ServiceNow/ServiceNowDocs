---
title: Mapping employees to their designated workspaces
description: Map your employees to their designated workplace locations in Workplace Core automatically to fill in that detail in reservation requests and to take advantage of auto-assignment of workspaces if that feature has been enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/mapping-employees-to-existing-work-locations-wsd.html
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

If you have installed Workplace Space Management application, as a Workplace manager, you can also view the reason for an anomaly in a workplace profile if there are any. A schedule job also enables you to view a detailed report of all the anomalies logged in the application via an email. Navigate to **Workplace Core** &gt; **Administration** &gt; **Workplace profiles** and switch to the Space Management view, a **Reason for anomaly** column appears as a Glide list. An anomaly can happen due to a mismatch in the allocation or assignment type. For more information about anomalies, see [Workplace location assignment anomaly types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/location-assignment-anomaly-types.md).

From Workplace Space Management 1.12.0, only open spaces from the user's allocation type that are within the allocation start and end dates are listed. After an allocation expires, the anomaly is recalculated to the appropriate value.

**Important:** Starting from Workplace Core version 2.16.1, the allocation type **Department and cost center** are no longer available. A new allocation type, **Workplace entity** is introduced that provides more advantages.

-   **[Map designated workspaces to user profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/map-employees-to-existing-workplace-locations-wsd.md)**  
Map existing designated workspaces to employee user profiles in Workplace Core. This mapping is used to automatically allocate workspaces for employees so they don't have to select a workspace manually when requesting a reservation.
-   **[Set the primary location of a workplace profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/set-prim-location-of-worplace-profile.md)**  
Assign a primary location for the workplace profile if there are multiple locations assigned.

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

[Assign the workplace user role to employees]()

[Configuring shifts for your workplace]()

[Managing workplace shifts that you own]()

[Managing workplace reservations for employees]()

[Setting and tracking arrivals at the workplace]()

[Approve employee workplace reservation requests]()

[Managing workplace tasks]()

[Workplace knowledge management]()

[QR code management]()

[Location migration]()

[View workplace service usage analytics with Usage Insights]()

