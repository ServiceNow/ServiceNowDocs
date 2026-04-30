---
title: Remap service portfolio taxonomy nodes in Service Portfolio Management
description: Use the flexible options when you remap \(or reparent\) taxonomy nodes from one portfolio to another. You can move an entire branch of a taxonomy from one portfolio to another, including the automatic move of its child nodes.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Edit and manage service portfolios in Service Portfolio Management, Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Remap service portfolio taxonomy nodes in Service Portfolio Management

Use the flexible options when you remap \(or reparent\) taxonomy nodes from one portfolio to another. You can move an entire branch of a taxonomy from one portfolio to another, including the automatic move of its child nodes.

## Before you begin

Role required: portfolio\_admin or service\_editor

## About this task

When you move taxonomy nodes from one portfolio to another, all its associated child nodes and their services and offerings move as well. This smooth transition confirms that your service portfolios are synchronized. Following the procedure, you may find it helpful to open the two portfolios in their own tab.

## Procedure

1.  Determine the service portfolio name that you want to add taxonomy nodes to.

2.  Open the service portfolio to take the taxonomy node from.

    -   Select the taxonomy node that you want to move.
    -   Change the **Service portfolio** field value to the name of the portfolio that you want to move the taxonomy node to. A message explains the impact of changing the portfolio name.
    -   Save the record.
    -   Refresh the Taxonomy Node list to see the updated portfolio display in the Service portfolio column.
3.  Verify the change in the DPM Workspace.

    -   Navigate to the Enterprise portfolios in the DPM Workspace.
    -   Find the portfolio that you added the taxonomy nodes to.
    -   Verify that the taxonomy nodes were added as well as their child nodes, services, and service offerings.
    **Important:** Service portfolios contain the Performance snapshot key performance indicator \(KPI\) values. If the KPI data is set to "latest score," the new node takes a day to reflect the updated KPI data. For more information, see [KPI groups in Digital Portfolio Management](../../digital-portfolio-management/concept/dpm-configure-kpi.md).


**Parent Topic:**[Edit and manage service portfolios in Service Portfolio Management](../concept/SPM2-edit-manage-portfolios.md)

