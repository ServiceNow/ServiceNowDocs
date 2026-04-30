---
title: Create taxonomy layer definitions
description: Create an unlimited number of taxonomy layers to organize, label, and manage your service portfolio. Taxonomy layers represent the highest containment levels of your service portfolio. Each level supports branches, or nodes, that contain child nodes or services in a hierarchical top-to-bottom structure.
locale: en-US
release: zurich
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Portfolio Management taxonomy, Create a portfolio, Use, Service Portfolio Management, IT Service Management]
---

# Create taxonomy layer definitions

Create an unlimited number of taxonomy layers to organize, label, and manage your service portfolio. Taxonomy layers represent the highest containment levels of your service portfolio. Each level supports branches, or nodes, that contain child nodes or services in a hierarchical top-to-bottom structure.

## Before you begin

**Important:** This task applies if you are using the legacy portfolio structure. For information on the legacy and standard portfolio structures, see [Service Portfolio Management taxonomy](../concept/SPM2-taxonomy.md).

Role required: portfolio\_admin

## About this task

Opening the **Taxonomy Layer Definitions** module displays a list of all existing layers defined for all service portfolios.

By default, the service portfolio name associated with the taxonomy layer is listed in the first **Service portfolio** column of the list. The service portfolio is the parent element to the taxonomy layer. Existing taxonomy layers appear in the **Name** column, and are chronologically sorted in the **Order** column. Your layer with order number 100 is always at the top, followed by order number 200, and so on.

Always associated taxonomy layers with a parent service portfolio. Example layers for an IT services portfolio might include the following taxonomy layers:

-   Service Class
-   Service Group

If the Service Portfolio Management Taxonomy Content Pack \[com.snc.spm.content\] plugin sample data is activated on your instance, review the provided taxonomy data to gain an understanding of how to best define your taxonomy layers. Refer to [Activate Service Portfolio Management Sample Content Pack](activate-SPM2-content-pack-plugin.md) for more details.

## Procedure

1.  Navigate to **Service Portfolio Management****Taxonomy Layer Definitions**.

2.  Select **New**.

    Alternatively, to edit an existing taxonomy layer definition, select the name of the taxonomy layer definition to open the form. Change any of the form field data as needed.

3.  Fill in or edit the form fields.

<table id="table_z5x_3lf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name that defines the purpose of the taxonomy layer, for example, Tier, as in software support tier or network support tier.

</td></tr><tr><td>

Order

</td><td>

Value that represents the hierarchical level where the taxonomy layer will exist. 1 is the highest level, with each chronological number following at a lower level.

**Note:** Layer ordering is locked and cannot be changed when a node is created for any layer in a service portfolio. Nodes cannot be added to layers if there is a gap in the layer order.

</td></tr><tr><td>

Service Portfolio

</td><td>

Service portfolio for which the taxonomy layer is associated.

</td></tr><tr><td>

Short description

</td><td>

Brief detail about the taxonomy layer purpose.

</td></tr></tbody>
</table>4.  Click **Submit** to save your service portfolio or click **Update** after editing a taxonomy layer.

5.  Click the newly created taxonomy layer definition in the list.

    The Taxonomy Nodes and Portfolio Metrics Related Lists appear on the Service Portfolio form. Refer to [Service Portfolio Management taxonomy](../concept/SPM2-taxonomy.md) for detailed information regarding creating and adding taxonomy nodes within your service portfolio structure.


**Parent Topic:**[Service Portfolio Management taxonomy](../concept/SPM2-taxonomy.md)

