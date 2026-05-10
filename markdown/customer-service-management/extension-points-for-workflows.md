---
title: Extension points for workflows
description: Override existing scripts or call custom scripts for the workflows by using extension points on the ServiceNow AI Platform.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Extension points for workflows

Override existing scripts or call custom scripts for the workflows by using extension points on the ServiceNow AI Platform®.

You can access the available extension points for the customer life cycle management workflows in the ServiceNow AI Platform®. Start by entering **sys\_extension\_point.list** in the application navigator and pressing **Enter**. Then, you can select the extension point that you want to view the record details of. If you want to override an existing script, you can select **Create implementation**.

You can create extension points so that you can create a workflow for a sold product extension that is not already configured. You can also override extension points to create configurations. To learn more about the existing extensions and configurations of the Customer Life Cycle Management Workflows, see [Customer Life Cycle Management Workflows](customer-life-cycle-management-workflows.md).

You can create several implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is the one that is executed.

The following table lists the extension points of the Customer Life Cycle Management Workflows.

<table id="table_u4t_rdd_d1c"><thead><tr><th>

Extension points

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CustomerWorkflowsEPsn\_l2c\_cust.flows.CustomerWorkflowEP

</td><td>

Overrides the existing flows and configurations.This extension can be used for any one of these two reasons:

-   If you want to execute custom flows that are extensions of the current sold product \(sn\_install\_base\_sold\_product\) table. To learn more about existing flows, see [Customer Life Cycle Management Workflows](customer-life-cycle-management-workflows.md).
-   If you want to execute custom Lead to Cash Core configurations. To learn more about existing Lead to Cash configurations, see [Entity configuration and mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/entity-configuration-and-mapping.md).

</td></tr><tr><td>

GetSoldProductClassEPsn\_l2c\_cust\_flows.GetSoldProductClassEP

</td><td>

Returns the correct sold product and product inventory class. The extension can be used to create custom flows in the **Add** and **Modify** flows.

</td></tr><tr><td>

CustomerWorkflowCompleteEPsn\_l2c\_cust\_flows.CustomerWorkflowCompleteEP

</td><td>

Overrides existing methods to perform any custom post-processing actions after an order to sold product flow is complete.

</td></tr></tbody>
</table>