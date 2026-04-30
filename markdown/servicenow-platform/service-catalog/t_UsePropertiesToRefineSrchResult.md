---
title: Refine search results
description: Use properties to refine search results in Service Catalog.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure search and navigation, Service Catalog home page configuration, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Refine search results

Use properties to refine search results in Service Catalog.

## Before you begin

Role required: admin

## About this task

The auto-completion feature returns values that contain an exact match to the letter combination entered.

Administrators can use the **Additional columns for the "request for" Service Catalog widget** \(glide.sc.request\_for.columns\) property to add columns to this list, to further refine the search results, and help determine which user to select when two users have the same name.

In this example, the property is set to display two additional columns, **Department** and **Title**:

Administrators can use the **Ordering of matches for the "request for" Service Catalog widget**. \(glide.sc.request\_for.order\_by\) property to configure the columns to sort by one of the values.

In this example, the is set to sort the results list by **department**.

Auto-completion also applies to the **Request for** field, which can be added to the service catalog homepage.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog**.

2.  Select **Add Categories**.

3.  Select **Request for**.

4.  Place the category on the page.


**Parent Topic:**[Configure search and navigation](../concept/c_ConfigSrchNavUseProps.md)

