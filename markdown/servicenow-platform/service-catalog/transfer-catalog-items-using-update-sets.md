---
title: Transfer catalog items using update sets
description: Transfer catalog items published through Catalog Builder from one instance to another easily by using update sets automatically created for the catalog item. For example, you can transfer catalog items created by a business user from a non-production to production instance.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Transfer catalog items using update sets

Transfer catalog items published through Catalog Builder from one instance to another easily by using update sets automatically created for the catalog item. For example, you can transfer catalog items created by a business user from a non-production to production instance.

## Before you begin

You can access update sets for a catalog item only if it is created or modified in Catalog Builder.

For information on creating a catalog item in Catalog Builder, see [Create a catalog item using a template](create-cat-item-template-cat-builder.md).

For information on editing a catalog item in Catalog Builder, see [Edit a catalog item in Catalog Builder](edit-cat-item-cat-builder.md).

Role required: catalog\_admin, catalog\_builder\_editor

## Procedure

1.  Access an update set for a catalog item by navigating to **All &gt; System Update Sets &gt; Local Update Sets**.

2.  Search for the update set by the name, `CB_<Template Name>_<Catalog Item Name>_<Date and Time Stamp>`.

    **Note:** If a catalog item contains related records such as Variables, Variable Sets, Available For, or Not Available For in a scope other than the current item scope, then such items are transferred in a batch where the related record update set's parent field is set as the update set of the parent catalog item. For more information, see [Update set batching](https://www.servicenow.com/docs/access?context=us-hier-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

3.  Transfer the completed update sets from the source instance to the target instance.

    For more information, see [Update set transfers](https://www.servicenow.com/docs/access?context=update-set-transfers&version=zurich&pubname=zurich-application-development&ft:locale=en-US).


**Parent Topic:**[Creating or editing catalog item template](create-cat-item-template-cat-builder.md)

