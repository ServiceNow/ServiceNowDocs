---
title: Catalog client script form
description: Use client-side scripts to define dynamic behavior or validations on this catalog item.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Edit a catalog item in Catalog Builder, Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog client script form

Use client-side scripts to define dynamic behavior or validations on this catalog item.

|Field|Description|
|-----|-----------|
|Actions|
|Name|Unique name for the catalog client script.|
|Active|Check box to enable the client script. Clear the check box to disable the script.|
|Select client script type|Select when the script runs, such as `onChange`, `onLoad`, or `onSubmit`.|
|Select question|Select a required question. This field is available only when you select `onChange` client script type.|
|Script|Enter the client script to run on the catalog item.|
|Settings|
|UI Type|Whether to apply this field to Desktop, Mobile or Service Portal, or all.|
|Order|Number representing a sequence.|
|Applies when the item is being requested|Check box to apply the catalog client script to catalog items displayed within the order screen on the portals. Available in the requester view.|
|Applies while viewing the requested item record after the request is submitted|Check box to apply the catalog client script on a Requested Item form, after the item is requested. Available in the fulfiller view. See [VEditor](../concept/service-catalog-variable-editor.md#cat-VEditor).|
|Applies while viewing the catalog tasks after the request is submitted|Check box to apply the catalog client script when a Catalog Task form for the item is being displayed. Available in the fulfiller view. See [VEditor](../concept/service-catalog-variable-editor.md#cat-VEditor).|

**Parent Topic:**[Edit a catalog item in Catalog Builder](edit-cat-item-cat-builder.md)

**Related topics**  


[Create client script in Catalog Builder](create-client-scripts-in-catalog-builder.md)

[Catalog builder developer \[catalog\_builder\_developer\]](../reference/r_ServiceCatalogManagementTermsandRoles.md#)

