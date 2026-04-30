---
title: Enable favorites option for Workplace Service Portal
description: Enable employees to set a workplace location as their favorite while using the Workplace Service Portal. Integrate with Employee Service Center to configure the favorites option.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Enable favorites option for Workplace Service Portal

Enable employees to set a workplace location as their favorite while using the Workplace Service Portal. Integrate with Employee Service Center to configure the favorites option.

## Before you begin

To enable the favorites option for Workplace Service Portal, verify that you have the latest versions of the following applications and plugins installed:

-   Employee Center Core \(sn\_ex\_sp\)
-   Employee Experience Taxonomy plugin \(sn\_ect\)
-   Employee Experience Foundation \(sn\_ex\_emp\_fd\)

Role required: esc\_admin or sn\_wsd\_core.admin

## About this task

Configure the favorites option so that employees can set any workplace location as their favorite. The employees can view their favorite locations anytime by selecting the **Favorites** tab on the Employee Center home page. The locations that they set as their favorite are given as the first priority when they search for available locations to make a reservation.

## Procedure

1.  Navigate to **All** &gt; **Favorites** &gt; **Favorite Content Configuration**.

2.  Verify that the following Content types are listed in the favorite Content Configuration form:

    -   Desks \(sn\_wsd\_core\_space\)
    -   Rooms \(sn\_wsd\_core\_rooms\)
3.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

4.  In the Service portals list, perform the following actions:

    1.  Go to **Workplace Services**.

    2.  In the **Enable favorites** column, set the option to **true**.


## Result

The favorites option is enabled for employees to set any workplace location as their favorite.

**Parent Topic:**[Manage workplace safety activities](../concept/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet](import-excel-spreadsheet-workspace-data-wsd.md)

[Add a space type configuration](add-space-type-configuration-wsd.md)

[Configure a workplace card](configure-workplace-card.md)

[Block a workplace location](block-workplace-location.md)

[Configure Workplace entity and entity types](../concept/workplace-entity.md)

[Create a workplace performer criteria](create-workplace-performer-criteria.md)

[Mapping employees to their designated workspaces](../concept/mapping-employees-to-existing-work-locations-wsd.md)

[Assign the workplace user role to employees](assign-workplace-user-role-to-employees-of-a-location-wsd.md)

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

