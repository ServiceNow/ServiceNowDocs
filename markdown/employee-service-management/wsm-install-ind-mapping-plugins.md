---
title: Install Workplace Indoor Mapping dependent plugins
description: Install the dependent plugins for Indoor Mapping.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Workplace Indoor Mapping, Configure, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Indoor Mapping dependent plugins

Install the dependent plugins for Indoor Mapping.

## Before you begin

Role required: admin

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view the required apps for integrating Indoor Mapping with Workplace Indoor Mapping.

**Note:** Install the Workplace Indoor Mapping Core plugin \(sn\_wsd\_indoor\_map\) in your ServiceNow instance before you install Indoor Mapping plugin \(sn\_map\_core\).

For cumulative release notes and information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for **Workplace Indoor Mapping** and **Indoor Mapping** in the application name using the filter criteria.

3.  Review the application dependencies.

    Install the dependent plugins before installing Indoor Mapping.

4.  The following dependent plugins must be installed to integrate Indoor Mapping with Workplace Service Delivery.

<table id="table_omv_jhb_btb"><thead><tr><th>

Dependent plugins

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Core \(sn\_wsd\_core\)

</td><td>

Provides workplace shift management and scheduling capabilities for workplace managers.

</td></tr><tr><td>

Workplace Space Mapping \(sn\_wsd\_space\_map\)

</td><td>

Provides space-mapping capabilities to support Workplace Service Delivery.**Note:** When Workplace Indoor Mapping is installed, it automatically installs Workplace Space Mapping.

</td></tr><tr><td>

Workplace Reservation Management \(sn\_wsd\_rsv\)

</td><td>

A universal reservation application offering unified reservation experience to your employees. The application enables employees to reserve rooms, desks, or any other workplace item at their desired time. You can view relevant information and services that are available for reservation at each location using Indoor Mapping maps.

</td></tr><tr><td>

Workplace Case Management \(sn\_wsd\_case\)

</td><td>

Workplace Case Management application that fulfills workplace service requests.

</td></tr><tr><td>

Workplace Move Management \(sn\_wsd\_move\)

</td><td>

Enables an employee to relocate from one location to another. Employees can collaborate, communicate, and easily manage space changes using the Workplace Service Portal.

</td></tr></tbody>
</table>
**Parent Topic:**[Configure Workplace Indoor Mapping](../concept/wsd-integration-indoor-mapping.md)

