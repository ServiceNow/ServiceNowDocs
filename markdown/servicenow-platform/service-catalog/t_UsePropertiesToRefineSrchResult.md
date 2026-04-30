---
title: Refine search results
description: Use properties to refine search results in Service Catalog.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure search and navigation, Service catalog home page configuration, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Refine search results

Use properties to refine search results in Service Catalog.

## Before you begin

Role required: admin

## About this task

The auto-completion feature returns values that contain an exact match to the letter combination entered.

![Auto-complete begins with first letter you type](../image/CatalogAutoComplete1.png "Catalog auto complete")

Administrators can use the **Additional columns for the "request for" Service Catalog widget** \(glide.sc.request\_for.columns\) property to add columns to this list, to further refine the search results, and help determine which user to select when two users have the same name.

In this example, the property is set to display two additional columns, **Department** and **Title**:

![Distinguish names by department](../image/CatalogAutoComplete2.png "Catalog auto complete using department")

Administrators can use the **Ordering of matches for the "request for" Service Catalog widget**. \(glide.sc.request\_for.order\_by\) property to configure the columns to sort by one of the values.

In this example, the is set to sort the results list by **department**.

![Results are ordered by department](../image/CatalogAutoComplete7.png "Catalog auto complete results by department")

Auto-completion also applies to the **Request for** field, which can be added to the service catalog homepage.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog**.

2.  Click **Add Categories**.

3.  Select **Request for**.

4.  Place the category on the page.

    ![Add a section in the catalog home page](../image/CatalogAutoComplete4.png "Add requested for catalog section")


**Parent Topic:**[Configure search and navigation](../concept/c_ConfigSrchNavUseProps.md)

