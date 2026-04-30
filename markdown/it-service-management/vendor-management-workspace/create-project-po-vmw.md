---
title: Create a Process Mining project for a KPI group
description: Create projects for each KPI group for which you want to mine the data.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Identifying bottlenecks using Process Mining integration with Vendor Management Workspace, Managing vendors using Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Create a Process Mining project for a KPI group

Create projects for each KPI group for which you want to mine the data.

## Before you begin

Your administrator must have enabled the **sn\_itsm\_vendor.enable.po.vm** system property to enable the mining. For more information on this system property, see [Installed with Vendor Management workspace](../reference/installed-w-vendor-manager-configurable-workspace.md).

Role required: sn\_process\_optimization\_analyst

## About this task

**Important:** The process mining projects for Vendor Management Workspace are created only for the incident table. Only templates of type **Default** are supported for creating the projects.

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Configuration** &gt; **KPI Groups**.

2.  Select a KPI group.

3.  Select **Initiate Process Mining**.

    The process mining is run on vendors within the KPI group and on all automated and formula indicators in the KPI group. If you're using a formula indicator for process mining, you can select any indicator source that is used in the formula.

    **Note:** When you select **Initiate Process Mining** and mine the vendor data for the first time, it creates the project and then adds the vendors to the project. When you add a KPI that is not part of the same table as the other KPIs, or if you add or remove vendors from the KPI group within this project, the changes are synchronized when the **Process Mining - VM Remine Projects** [scheduled job](../reference/installed-w-vendor-manager-configurable-workspace.md) runs the next time. You can also select **Initiate Process Mining** and run it to synchronize the changes immediately.

    A corresponding project is created in the **All** &gt; **Vendor Management** &gt; **Configuration** &gt; **VM Projects** module. When the mining is complete, the **Mining state** field changes to **Available**.

    When you navigate to **Vendor Management** &gt; **Configuration** &gt; **Process Mining Project Mapping**, you can see the relationship between the indicator, KPI group, project definition, and the table for the project you've mined.


**Parent Topic:**[Identifying bottlenecks using Process Mining integration with Vendor Management Workspace](use-process-optimization-vmw.md)

