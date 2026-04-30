---
title: Redirect WSD RSV MOA OAuth registry
description: Redirect MOA Outh access \(moa\_login\) for Microsoft Outlook Add-in version 1.12.2 or earlier to WSD RSV MOA OAuth registry \(rsv\_moa\_login\) registry.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 2
breadcrumb: [Manage Workplace Reservations for Microsoft Outlook Add-in, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Redirect WSD RSV MOA OAuth registry

Redirect MOA Outh access \(moa\_login\) for Microsoft Outlook Add-in version 1.12.2 or earlier to WSD RSV MOA OAuth registry \(rsv\_moa\_login\) registry.

## Before you begin

Workplace users using Microsoft Outlook Add-in version 1.12.2 or earlier versions, can migrate to Workplace Reservation Management 3.0.2. After migrating, redirect the MOA OAuth registry \(moa\_login\) to WSD RSV MOA OAuth registry \(rsv\_moa\_login\).

Workplace Reservation Management 3.0.2 Microsoft Outlook Add-in capabilities provide enhanced reservation experience for employees. For more information, see [Manage Workplace Reservations for Microsoft Outlook Add-in](../concept/manage-outlook-addin-rsv.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Services Portal** &gt; **Page Route Map**.

2.  Select **WSD Microsoft Outlook Add-in**.

    The Page Route Map form opens. By default, all field values are preloaded in the Page Route Map form. Select the edit option to edit the form.

    ![Page Route map to redirect from existing Microsoft Outlook Add-in login to Workplace Reservation Management.](../image/outlook-page-route-map-form-details.png)

    |Field|Description|
    |-----|-----------|
    |Short Description|Optional short description to describe the redirect.|
    |Service Portal\(s\)|Portals that apply the redirect. If you don't select a portal, the redirect applies to all portals in the instance.|
    |Route from|Original page you’re redirecting from. For example, **moa\_login**.|
    |Route to|Page you’re redirecting to. For example, **rsv\_moa\_login**.|
    |Active|Page Route Map record is active or inactive. The redirect from **moa\_login** to **rsv\_moa\_login** happens when the record is active.|
    |Roles|Roles to which the page route map applies. Employees that don't have any of the roles specified in this field aren't redirected to the new page. If no roles are specified, the page route map is applicable to all users.|
    |Order|Priority of the Page Route Map record. If more than one active record has the same value in the **Route from** field, the record with the lowest order applies. The system evaluates records from lowest to highest. If multiple records have a matching order, the system prioritizes the oldest record.|

3.  Select or clear the **Active** check box.

    The **Active** check box is selected by default.

    When the **Active** check box is selected, MOA OAuth registry \(moa\_login\) is redirected to WSD RSV MOA OAuth registry \(rsv\_moa\_login\) in Workplace Reservation Management 3.0.2 version.

    **Note:** If you don’t want to redirect and update to rsv\_moa\_login and opt to use Microsoft Outlook Add-in 1.12.2 or earlier versions MOA OAuth registry \(moa\_login\), clear the **Active** check box.

4.  Select **Update** to save the changes you made to the Page Route Maps form.

    All references in the **Route from** field redirect to the page in the **Route to** field.


