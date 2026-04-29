---
title: Classification codes
description: Use classification codes to organize and categorize your enterprise models and use them effectively.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Classification codes

Use classification codes to organize and categorize your enterprise models and use them effectively.

## Overview of classification codes

Create classification codes to increase the visibility and efficiency of your enterprise models. For details, see [Create sources for classification codes](../task/create-class-source-eam.md).

You can also import multiple classification codes at one go to your ServiceNow instance. For details, see [Import classification codes](../task/import-class-codes-eam.md).

Classification codes are assigned to models, are based on model categories, and each code has a source.

A classification code can be based on one or more model categories. For example, the facility model category is assigned to Code A and the medical model category is assigned to Code B. You can assign a code to each model you create. When you create a facility model, you can assign the classification code, Code A to that model. Similarly, when you create a medical model, you can assign Code B to that model.

A source is a system of classification for a particular industry. OmniClass, for example, is a classification system for the construction sector. Some sources have a hierarchical structure with a parent-child relationship. In such a hierarchical system, there's only one parent for each code. Your data infrastructure determines whether a source adheres to a hierarchical structure or not. For details, see [Create sources for classification codes](../task/create-class-source-eam.md).

Use the parent-child relationship between models to filter out models and assets based on a classification code. You can filter reports on dashboards based on classification codes.

You can create and edit classification codes in the Enterprise Asset Workspace by navigating to **Enterprise model management view** &gt; **Classification**.

When a classification code is created, the ancestor list for that code is generated automatically. When a parent of an existing code is updated, the ancestor list of that code and all its children gets updated.

## Filter using classification codes

You can filter models based on classification codes in the following Enterprise Asset Workspace views:

-   Enterprise asset overview
-   Enterprise asset dashboard
-   Inventory
-   Enterprise model management
-   Enterprise asset estate

When you select a code in the **Classification** filter and apply the filter, you see reports for all the models aligned to that code, as well as all their ancestors.

## Roles used

You need the following roles to work with classification codes.

<table id="table_zts_fw2_rwb"><thead><tr><th>

Role title

</th><th>

Contains roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Classification manager \[sn\_eam.enterprise\_classification\_manager\]

</td><td>

sn\_eam.enterprise\_admin

</td><td>

This role has complete access to the classification code table. This role can create classification codes as well as edit and view them.

</td></tr><tr><td>

Model manager \[model\_manager\]

</td><td>

sn\_eam.enterprise\_asset\_manager

</td><td>

This role can only view classification codes.

</td></tr></tbody>
</table>