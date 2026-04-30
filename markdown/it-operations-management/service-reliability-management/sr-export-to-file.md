---
title: Export list information to a file
description: You can export live information to a file in Service Reliability Management \(SRM\).This is the file referenced by all lists that can export. No need for services, alerts, incident or calendar specific files. They are kept in repo until certain about this.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SRM interface, Get started with Service Reliability Management, Exploring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Export list information to a file

You can export live information to a file in Service Reliability Management \(SRM\).

## Before you begin

**Note:** Bulk selection doesn't impact exports. The export includes all records that match the current filter criteria. It doesn't consider the selections you make in the list view.

Role required: srm\_admin, srm\_manager, or srm\_responder

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

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
    For **Email**: Once the export is complete, a success message appears with your email address at the top of the screen. It's useful for larger files because, depending on the size of the file, exporting might take some time. Email runs in the background, so you’re free to do something else while waiting.

    For **Download**: The pop-up begins exporting and the file appears in your Download directory. Depending on the size of the file, it might take some time. You can open it in any application that supports the file format.


**Parent Topic:**[SRM interface](../concept/sr-navigate-interface.md)

