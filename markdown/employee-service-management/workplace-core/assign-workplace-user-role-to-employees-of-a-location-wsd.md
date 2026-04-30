---
title: Assign the workplace user role to employees
description: Set rules in Workplace Core to assign the workplace user role to employees and apply conditions accordingly.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Assign the workplace user role to employees

Set rules in Workplace Core to assign the workplace user role to employees and apply conditions accordingly.

## Before you begin

Ensure that the user profiles of all your employees have required details. You can review the employee user profiles by navigating to **User Administration** &gt; **Users**.

Role required: admin or sn\_wsd\_core.admin

## Procedure

1.  Navigate to **Workplace Safety Management** &gt; **Administration**.

2.  Select **Client Role Assignment Rules**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for this assignment rule.|
    |Role|This value is auto-generated with the workplace user role \(sn\_wsd\_core.workplace\_user\).|
    |Active|Option for indicating whether this assignment rule is active.|
    |Condition|Option to add filter conditions that a user profile must match. To add a condition, select **Add filter condition**. To add a OR clause, select **Add "OR" clause**.|
    |Table|Table on which the conditions must be built. The field is automatically selected as `sys_user`.|

4.  Select **Submit**.


## Result

The workplace user roles are assigned. If a record is created or updated on this table, a role assignment process is triggered in the background.

**Parent Topic:**[Manage workplace safety activities](../concept/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet](import-excel-spreadsheet-workspace-data-wsd.md)

[Add a space type configuration](add-space-type-configuration-wsd.md)

[Configure a workplace card](configure-workplace-card.md)

[Block a workplace location](block-workplace-location.md)

[Configure Workplace entity and entity types](../concept/workplace-entity.md)

[Managing Neighborhoods](../../workplace-space-management/concept/neighborhoods.md)

[Enable favorites option for Workplace Service Portal](confgure-favourites-option-for-ws-portal-wsd.md)

[Create a workplace performer criteria](create-workplace-performer-criteria.md)

[Mapping employees to their designated workspaces](../concept/mapping-employees-to-existing-work-locations-wsd.md)

[Configuring shifts for your workplace](../concept/configuring-shifts-for-your-workplace-wsd.md)

[Managing workplace shifts that you own](../concept/managing-shifts-you-own-wsd.md)

[Managing workplace reservations for employees](../concept/managing-workplace-reservations-wsd.md)

[Setting and tracking arrivals at the workplace](../concept/scheduling-employees-arrival-to-the-workplace-wsd.md)

[Approve employee workplace reservation requests](approve-workplace-reservation-requests-wsd.md)

[Managing workplace tasks](../concept/managing-workplace-maintenance-tasks.md)

[Workplace knowledge management](../concept/workplace-knowledge-mgmt-wsd.md)

[QR code management](../concept/qr-code-mgmt.md)

[Location migration](../concept/location-migration.md)

[View workplace service usage analytics with User Experience Analytics](../reference/appsee-intergration-wsd.md)

