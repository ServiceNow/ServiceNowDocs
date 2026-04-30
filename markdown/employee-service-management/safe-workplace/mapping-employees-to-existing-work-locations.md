---
title: Mapping employees to their designated workspaces
description: Map your employees to their designated workplace locations in Workplace Core to automatically fill in that detail in reservation requests and to take advantage of auto-assignment of workspaces if that feature has been enabled.
locale: en-US
release: zurich
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Mapping employees to their designated workspaces

Map your employees to their designated workplace locations in Workplace Core to automatically fill in that detail in reservation requests and to take advantage of auto-assignment of workspaces if that feature has been enabled.

For employees who had a designated workspace before they started working remotely, create a mapping between the user profile and the designated workspace details. This mapping populates the workspace details on reservation request forms so employees don't have to provide these details manually.

If your system administrator has enabled the auto-assign feature, mapping workspaces for all employees also means that designated workspaces are automatically assigned when employees make a reservation request.

The data from the User Workplace Profile \[sn\_wsd\_core\_workplace\_profile\] table is used to automatically assign the designated workspace to the employee.

-   If the user's designated space is available, this space is reserved for the employee.
-   If the designated space is unavailable for the requested date or time, the application searches for and reserves an available space in the employee's workplace in the order of Area &gt; Floor &gt; Building &gt; Campus &gt; Site &gt; Region.

    For example, if no spaces are available in the designated area of the employee, the application finds and reserves an available space from the floor of this area.


-   **[Map designated workspaces to user profiles](../task/map-employees-to-existing-workplace-locations-hr.md)**  
Map existing designated workspaces to employee user profiles in Workplace Core. This mapping is used to automatically allocate workspaces for employees so they don't have to select a workspace manually when requesting a reservation.

**Parent Topic:**[Workplace Core](workplace-safety-mgmt-hr.md)

