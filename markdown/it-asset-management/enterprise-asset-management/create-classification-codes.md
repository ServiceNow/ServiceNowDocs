---
title: Create classification codes
description: Create classification codes and assign them to enterprise models and model categories to increase the efficiency of enterprise models.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise models, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create classification codes

Create classification codes and assign them to enterprise models and model categories to increase the efficiency of enterprise models.

## Before you begin

Each classification code is assigned to one or many model categories. Classification codes are stored in the Enterprise model classification \[sn\_ent\_model\_classification\] table.

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Enterprise model management** &gt; **Classification**.

2.  Select **New**.

3.  On the form, fill in the details.

<table id="table_vkt_jhj_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Classification

</td><td>

The display name of the classification code record which is automatically generated after the record is saved.

 The display name is a concatenation of the classification code, its description, and the source.

</td></tr><tr><td>

Code

</td><td>

The classification code.

 Based on your data infrastructure, the code may adhere to a hierarchical structure.

</td></tr><tr><td>

Description

</td><td>

Description of the classification code.

</td></tr><tr><td>

Parent

</td><td>

Parent of the classification code. If you select a parent, the model categories assigned to the parent code are automatically populated in the **Model categories** field. This field is however editable. You can delete a model category that is automatically populated or you can add another model category.

</td></tr><tr><td>

Source

</td><td>

The source system that a classification code is based on. For example, OmniClass is a classification system for the construction industry.

</td></tr><tr><td>

Model categories

</td><td>

Mode categories assigned to the code.

</td></tr></tbody>
</table>4.  Select **Save**.

    The display name of the classification code is generated and displayed in the **Classification** field. The display name represents the code, the description, and the source. You can view the new classification code record in the Classifications list view page.


**Parent Topic:**[Create and manage enterprise models](../concept/create-manage-enterprise-models.md)

