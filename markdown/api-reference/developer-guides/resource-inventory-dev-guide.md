---
title: Resource Inventory Open API Developer Guide
description: Use the Resource Inventory Open API to create, retrieve, update, and delete resources such as interface cards, logical and physical connections, network sites, and more.The Resource Inventory Open API can be extended using extension points and script includes.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Developer guides, API implementation and reference]
---

# Resource Inventory Open API Developer Guide

Use the Resource Inventory Open API to create, retrieve, update, and delete resources such as interface cards, logical and physical connections, network sites, and more.

This developer guide provides information on how to extend the [Resource Inventory Open API](../../../inbound-rest/concept/resource-inventory-api.md#) to make various customizations.

## Extending the Resource Inventory Open API

The Resource Inventory Open API can be extended using extension points and script includes.

### Extension points

The Resource Inventory Open API includes extension points that can be used to modify the existing schema for the API, which defines required parameters. Extension points can also be used to add new parameters and map them to fields on the ServiceNow AI Platform, or to change the mapping for existing parameters. For example, you can add new resource characteristics and map them to the appropriate fields.

The following extension points are included with the Resource Inventory Open API.

-   `TNITMFResourceInventoryAPICreateResource`: Extension point to create a resource.
-   `TNITMFResourceInventoryAPIPatchResource`: Extension point to update a resource.
-   `TNITMFResourceInventoryAPITransformToIREPayload`: Extension point to create an Identification and Reconciliation engine \(IRE\) payload from a TMF request.
-   `TNITMFResourceInventoryAPITransformToResponse`: Extension point to create a TMF response from a resource GlideRecord.
-   `TNITMFResourceInventoryAPIValidateCreate`: Extension point to validate a TMF POST request.
-   `TNITMFResourceInventoryAPIValidatePatch`: Extension point to validate a TMF PATCH request.

### Script includes

Use script includes to override the default validation and transformation functions. Default functions are defined in the `sn_ni_core.TNITMFResourceInventoryProcessorOOB` script include. To override the default functions, create functions with identical names and parameters in the `sn_ni_core.TNITMFResourceInventoryProcessor` script include.

