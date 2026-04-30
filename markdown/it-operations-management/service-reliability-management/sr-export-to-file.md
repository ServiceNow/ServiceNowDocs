---
title: Export list information to a file
description: You can export live information to a file in SRM.This is the file referenced by all lists that can export. No need for services, alerts, incident or calendar specific files. They are kept in repo until certain about this.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SRM interface, Get started with Service Reliability Management, Exploring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Export list information to a file

You can export live information to a file in SRM.

## Before you begin

**Note:** Bulk selection has no affect on export criteria and should not be used for it. Any record that matches the current filter criteria during export will be included, regardless of whether or not it is selected in the list view.

Role required: Responder, Manager, or Administrator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  Select the list view in any landing page section in SRM with an **Export button**.

3.  Determine which filters you want to use and select them from the Filters ![Filter icon.](../image/icon-sr-filter.png) or More actions menu in the list columns.

    **Note:**

    The Export button only becomes available if there are records in the list view.

    The export contains all list data that matches your filtered/grouped lists.

4.  Select **Export**.

    In the pop-up window select:

    -   File Type:
        -   Excel
        -   CSV
        -   JSON
        -   PDF
    -   Delivery type:
        -   Download
        -   Email: Provide an email address
    For **Email**: Once the export is complete, a success message appears with your email address at the top of the screen. It's useful for larger files because, depending on the size of the file, exporting may take some time. Email runs in the background, so you’re free to do something else while waiting.

    For **Download**: The pop-up begins exporting and the file appears in your Download directory. Depending on the size of the file, this may take some time. You can open it in any application that supports the file format.


**Parent Topic:**[SRM interface](../concept/sr-navigate-interface.md)

