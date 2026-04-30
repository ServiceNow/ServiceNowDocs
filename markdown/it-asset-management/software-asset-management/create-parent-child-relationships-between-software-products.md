---
title: Create parent-child relationships between software products
description: Create and define the parent-child relationships between your software products so that your child products can inherit life-cycle dates from their parent products.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create parent-child relationships between software products

Create and define the parent-child relationships between your software products so that your child products can inherit life-cycle dates from their parent products.

## Before you begin

Role required: sam\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  From the Software Asset Workspace, open the License operations view.

3.  From the navigation menu of the License operations view, navigate to **Content** &gt; **Parent-Child Relationship**.

4.  Select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Parent product|Parent product that the specified child product inherits life-cycle dates from.|
    |Child product|Child product that inherits life-cycle dates from the specified parent product. If you leave this field empty, a blanket parent-child relationship is created, in which all products under the same publisher as the specified parent product are considered its children and inherit its life-cycle dates.|
    |Active|Option that indicates if the parent-child relationship is active.|
    |Exclusion|Option to exclude the specified child product from any existing blanket parent-child relationships that are defined using the specified parent product.|

6.  Select **Save**.


## Result

The Software Asset Management application automatically updates the life-cycle dates of the specified child product with the life-cycle dates of the specified parent product, given that the child product does not already have its own specific life-cycle dates.

## What to do next

View life-cycle dates and other life-cycle information for both your parent and child software products in the Lifecycle management dashboard. You can access this dashboard by navigating to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Lifecycle management**. See [Lifecycle management dashboard](../concept/lifecycle-management-dashboard.md) for more information on this dashboard.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

