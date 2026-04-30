---
title: Set up Platform URLs for catalog modules
description: You can direct users to a specific catalog via a URL to a module in that particular catalog.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service catalog setup, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up Platform URLs for catalog modules

You can direct users to a specific catalog via a URL to a module in that particular catalog.

## Before you begin

Role required: admin

## About this task

When you create a module for your catalog page, you can direct users to a specific catalog and view from this module via a URL.

## Procedure

1.  In the **Link Type** section, select **URL \(from Arguments\)**, then in the **Arguments** field, enter a URL of the form `catalog_home.do?sysparm_catalog=id of sc_catalog record&sysparm_catalog_view=view name of sys_portal_page`.

    For example, `catalog_home.do?sysparm_catalog=742ce428d7211100f2d224837e61036d&sysparm_catalog_view=catalog_technical_catalog`

    **Note:** If you make the default catalog inactive, then deactivate the **Catalog** module otherwise users can continue to access the inactive catalog using that module.

    If a URL has a valid **sysparm\_catalog**parameter, but an invalid or missing **sysparm\_catalog\_view** parameter, the view with the default value from the corresponding Catalog Portal Page record is used.

    If a URL has a valid **sysparm\_catalog\_view** parameter, but an invalid or missing **sysparm\_catalog** parameter, the corresponding Catalog Portal Page record is used to set the catalog.

    **Note:** To ensure peak performance, define both parameters correctly.


**Parent Topic:**[Service catalog setup](../topic/p_ServiceCatalogs.md)

