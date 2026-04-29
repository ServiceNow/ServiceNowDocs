---
title: Integrate with the UKG spoke
description: Integrate with the UKG spoke to use the Employee Center Pro Kiosk in your organization.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Employee Center Pro Kiosk, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Integrate with the UKG spoke

Integrate with the UKG spoke to use the Employee Center Pro Kiosk in your organization.

## Before you begin

Activate the following plugins in their required versions or later versions to use the Employee Center Pro kiosk.

-   Activate Employee Center Pro plugin version 31.0.4 \(sn\_ex\_sp\_pro\).
-   Activate Employee Profile plugin version 11.0.3 \(sn\_employee\).
-   Activate the HR Service Delivery with Ultimate Kronos Group plugin \(sn\_hr\_ukg\).

**Note:** Installation of the HR Service Delivery with Ultimate Kronos Group plugin \(com.sn\_hr\_ukg\) provides a default setup of the UKG spoke.

Role required: admin

## About this task

If you don't plan to activate the HR Service Delivery with Ultimate Kronos Group plugin \(com.sn\_hr\_ukg\), Set up the UKG spoke manually. The HR UKG integration plugin provides you with a default Kronos integration.

## Procedure

1.  Set up the UKG spoke.

    -   For more information on the setup, see [Set up the](https://www.servicenow.com/docs/access?context=setup-kronos&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
    -   The schedule and time off data on the Employee Center Pro kiosk is enabled with the existing UKG spoke actions.
        -   **Look up Employee Schedule**: To get the shift schedule data.
        -   **Get Employee Accruals by Person Number**: To get the time off balance data.

            For more information on creating requests, see [Create request as manager using the catalog item](https://www.servicenow.com/docs/access?context=kronos-serv-cat&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).


-   **[Receive employee data from UKG to the Employee Center Pro Kiosk](user-map-kronos-kiosk.md)**  
Map the employee IDs between the UKG system and the Employee Center Pro Kiosk to see employee details in your organizational kiosks.

**Parent Topic:**[Employee Center Pro Kiosk](../concept/deskless-kiosk-overview.md)

