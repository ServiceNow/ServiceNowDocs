---
title: Universal Request roles and groups
description: Users with certain roles and access can use Universal Request.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Universal Request, Universal Request, Employee Service Management]
---

# Universal Request roles and groups

Users with certain roles and access can use Universal Request.

|Role|Description|
|----|-----------|
|sn\_uni\_req.universal\_request\_read|Users with this role have read access to the Universal Request application and the related functions.|
|sn\_uni\_req.ur\_admin|UR administrators can setup and configure Universal Request.|
|sn\_uni\_req.routing\_agent|Users with this role can open, update, and close Universal requests. By default, the users with the sn\_uni\_req.routing\_agent role alone can have Universal requests assigned to them.|
|sn\_uni\_req.universal\_request\_write|Users with this role have both read and write access to the Universal Request application and the related functions.|
|sn\_uni\_req.ur\_service\_owner|Users with this role act as the Universal Request service owner that defines the process to service the universal request.|
|sn\_uni\_req.sensitiveinfo\_agent|Users with this role can view and work on the tickets that are marked as restricted. Restricted tickets contain sensitive information and are secured from general viewing.|

Universal Request application provides the following default assignment groups as part of the demo data. You can customize the default groups or create your organization-specific assignment groups.

<table id="table_gqh_swg_llb"><thead><tr><th>

Group

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IT Routing group

</td><td>

Assignment group that consists of tier-1 agents who manage both Universal Requests and IT incidents. The agents of this assignment group have both Universal Request role and the ITIL role. Agents assigned to the IT Routing group can:-   Manage Universal Request.
-   Create child IT incidents from the UR parent.

</td></tr><tr><td>

HR Routing group

</td><td>

Assignment group that consists of tier-1 agents who manage both Universal Requests and HR cases. The agents of this assignment group have both Universal Request role and the HR role. Agents assigned to the HR Routing group can:-   Manage Universal Request
-   Create child HR cases from the UR parent.

</td></tr><tr><td>

Universal Request Routing group

</td><td>

Assignment group that consists of tier 1 agents who focus primarily on managing Universal Requests. The agents of this assignment group have Universal Request role. Agents assigned to the Universal Request Routing group can:-   Resolve the Universal Request at the parent level.
-   Assign the Universal Request to another assignment group, such as HR routing group or IT routing group.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Universal Request](explore-universal-request.md)

