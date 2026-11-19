---
title: Deactivate a connection
description: Temporarily disable the connection between data fabric tables and their data source by deactivating a connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/deactivate-connnection-zcc.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Update an established connection, Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Deactivate a connection

Temporarily disable the connection between data fabric tables and their data source by deactivating a connection.

## Before you begin

Role required: df\_connection\_admin

## About this task

A connection admin can stop queries to an external data source or prevent changes to data mapping by deactivating a connection. When a connection is deactivated, external data isn't available from any data fabric tables using the connection.

## Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to deactivate.

3.  Select the More Actions icon \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions icon\), and select **Deactivate**.

4.  Confirm that you want to deactivate the connection by selecting **Deactivate**.


## Result

The connection is deactivated.

-   External data is no longer pulled by any data fabric table using the connection.
-   The **Data Assets** tab and **Access Control** tabs aren't accessible in the connection.

## What to do next

To update the connection information or access the **Data Assets** or **Access Control** tabs again, you must reactivate the connection. See [Reactivate a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/reactivate-connnection-zcc.md).

**Parent Topic:**[Update an established connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/configure-connection-details-zcc.md)

