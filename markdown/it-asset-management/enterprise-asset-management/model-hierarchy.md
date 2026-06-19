---
title: Model categories
description: Model categories define the relationships between enterprise model classes, enterprise asset classes, and Configuration Management Database \(CMDB\) CI classes in Enterprise Asset Management. Model categories connect every enterprise asset to the correct model class, asset class, and CI class.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/model-hierarchy.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enterprise Asset Management data model, Explore, Enterprise Asset Management, IT Asset Management]
---

# Model categories

Model categories define the relationships between enterprise model classes, enterprise asset classes, and Configuration Management Database \(CMDB\) CI classes in Enterprise Asset Management. Model categories connect every enterprise asset to the correct model class, asset class, and CI class.

## Overview of model categories

When you create an enterprise model, you assign it to a model category. The assignment determines:

-   The model class for the model record
-   The asset class for assets created from that model
-   The CI class for the corresponding CMDB CI record

\[Omitted image "modelcategory.png"\] Alt text: Model category

Model category assignments follow these rules:

-   Multiple model categories can share the same model class or asset class.
-   A CI class can be assigned to only one model category, and this assignment is optional.

## Model category functions

Beyond routing records into the correct classes, model categories serve three purposes:

1.  Asset and CI record creation: EAM uses the model category to place assets in the correct asset class and create linked CI records in the correct CI class.
2.  Bi-directional asset-CI synchronization: The model category mapping keeps asset and CI records in sync. Changes to state, location, or assignment are reflected in both records.
3.  Discovery and identification rules: Model categories use configured CMDB IRE rules to define asset unique identifiers. These identifiers determine how the system recognizes assets when data arrives from Discovery or Procurement.

## Parent and child model categories

Model categories are organized in a two-tier hierarchy. Parent model categories represent the nine top-level industry domains. Child model categories sit beneath a parent and carry the actual class mappings assigned to model records.

\[Omitted image "parent\_model\_eam.png"\] Alt text: The 9 seeded parent model categories: Medical, Facility, Transportation, Industrial, Multimedia production equipment, Retail, Construction, Tactical equipment, and Wearable

For the complete list of available model categories and their corresponding CMDB CI class, asset class, and model class, see [Enterprise model categories and corresponding classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-model-categories.md).

**Important:** Use only the existing top-level parent model categories.

## Creating custom model categories

If none of the existing child model categories meet your needs, you can create a custom child category under an existing parent. When creating a child category, you specify the parent model category, model class, asset class, and optionally a CI class. For details, see [Create model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/create-custom-model-category.md)

**Important:**

Custom model categories must be children of one of the nine seeded parent categories. Creating new top-tier parent categories is not supported.

**Parent Topic:**[Enterprise Asset Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md)

