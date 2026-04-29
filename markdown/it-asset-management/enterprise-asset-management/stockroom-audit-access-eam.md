---
title: Stockroom audit access by role
description: Audit roles determine which stockrooms a user can view and audit. Depending on your application and assigned role, you may have access to all stockrooms or only personal stockrooms.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 1
keywords: [Stockroom audit in EAM, Audit roles in EAM]
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Stockroom audit access by role

Audit roles determine which stockrooms a user can view and audit. Depending on your application and assigned role, you may have access to all stockrooms or only personal stockrooms.

## Stockroom audit roles

|Role|Stockroom scope|Read|Write|Create|Delete|
|----|---------------|----|-----|------|------|
|sn\_itam\_common.personal\_stockroom\_audit\_user|Assigned personal stockrooms only|Yes|Yes|Yes|No|
|sn\_itam\_common.personal\_stockroom\_audit\_admin|Personal stockrooms only|Yes|Yes|Yes|Yes|
|sn\_itam\_common.asset\_audit\_user|All stockrooms|Yes|Yes|Yes|No|
|sn\_itam\_common.asset\_audit\_admin|All stockrooms|Yes|Yes|Yes|Yes|

**Important:** Access to the Asset Audits \[sn\_itam\_common\_asset\_audit\] table is no longer granted through the inventory\_user role. Assign one of the new audit roles to users who require audit access.

## Role hierarchy

The audit roles are organized in the following hierarchy:

-   The sn\_itam\_common.asset\_audit\_user role is contained within the sn\_itam\_common.asset\_audit\_admin role.
-   The sn\_itam\_common.personal\_stockroom\_audit\_user role is contained within the sn\_itam\_common.personal\_stockroom\_audit\_admin role.

## Role assignments by application

-   **Enterprise Asset Management**
    -   The sn\_eam.asset\_technician role is assigned the sn\_itam\_common.asset\_audit\_user role, enabling read, write, and create access on all stockrooms.
    -   The sn\_eam.enterprise\_admin role is assigned the sn\_itam\_common.asset\_audit\_admin role, enabling full access to all stockroom and location audits, including the ability to delete audit records.
-   **Hardware Asset Management**

    The ham\_admin role is assigned the sn\_itam\_common.asset\_audit\_admin role, enabling full access on all stockrooms.

    **Note:** For more details on stockroom auditing in the Hardware Asset Management application, see [Audit hardware asset inventory](../../hardware-asset-management/concept/ham-inventory-audit.md).

-   **Field Service Management**

    -   The wm\_agent is assigned the sn\_itam\_common.personal\_stockroom\_audit\_user role, restricting access to personal stockrooms only.
    -   The wm\_admin role receives full access including delete through sn\_itam\_common.personal\_stockroom\_audit\_admin.
    **Note:** For more details on stockroom auditing in the Field Service Management application, see [Perform asset audit for personal stockrooms](https://www.servicenow.com/docs/access?context=perform-asset-audit&version=australia&pubname=australia-field-service-management&ft:locale=en-US).


-   **[Audit enterprise asset inventory](../task/audit-eam-assetinventory.md)**  
Audit your enterprise asset inventory to learn where your assets are and what their current status is.

**Parent Topic:**[Create and manage enterprise asset inventory](managing-enterprise-asset-inventory.md)

