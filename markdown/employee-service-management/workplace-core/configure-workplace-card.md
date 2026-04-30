---
title: Configure a workplace card
description: Create a workplace card to be used in your workplace applications.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 5
breadcrumb: [Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configure a workplace card

Create a workplace card to be used in your workplace applications.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

Card configuration enables admins to tailor the display and functionality of space cards across modules like Reservation, Location Directory, and Kiosk Indoor Mapping. You can control visible fields and available actions like reserving a space or copying a URL. You can also add multiple card configurations to a single page, using conditions to determine which card is displayed.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Card configuration**.

2.  On the Workplace Card Configurations list, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the card configuration.|
    |Template|UI template that is used for the card. You can use existing templates or create your own by using UI macros. For more information, see [UI macros](https://www.servicenow.com/docs/access?context=c_UIMacros&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).|
    |Order|Order of the card configuration.|
    |Table|Table that is used to generate the fields on the card.|
    |Applications|Applications that use the card configuration. You can select Location Directory, Reservation, and Kiosk Indoor Mapping.|

4.  Add conditions for the card configuration.

    The conditions determine where the card is displayed in the selected applications. For example, if the table is `Space [sn_wsd_core_space]` and the condition is `Active is true`, the card is displayed only for active spaces.

    The fields in the condition builder are fetched from the selected table. For more information about the condition builder, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

5.  Select **Submit**.


-   **[Configure a space details card](configure-a-space-details-card.md)**  
Configure a space card in the Location Directory, Kiosk Indoor Mapping, or Reservation by updating the card's template with the specific details that you want to customize. You can configure a new field, button, or style for each space card.

**Parent Topic:**[Manage workplace safety activities](../concept/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet](import-excel-spreadsheet-workspace-data-wsd.md)

[Add a space type configuration](add-space-type-configuration-wsd.md)

[Block a workplace location](block-workplace-location.md)

[Configure Workplace entity and entity types](../concept/workplace-entity.md)

[Managing Neighborhoods](../../workplace-space-management/concept/neighborhoods.md)

[Enable favorites option for Workplace Service Portal](confgure-favourites-option-for-ws-portal-wsd.md)

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

