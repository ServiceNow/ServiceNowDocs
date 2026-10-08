---
title: Map a dashboard to a partition
description: Give a partition its own dashboard for an experience, such as Demand Management, so that users who select the partition see the dashboard mapped to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/map-dashboard-to-partition-ewd.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Map a dashboard to a partition

Give a partition its own dashboard for an experience, such as Demand Management, so that users who select the partition see the dashboard mapped to it.

## Before you begin

-   Make sure the partition that you want to map the dashboard to exists. For details, see [Create and configure a partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/create-partition-ewd.md).
-   Make sure the **Experience** field is set to **Strategic Planning Workspace** in the PAR Dashboard Visibility \[par\_dashboard\_visibility\] table for the dashboard that you want to map to the partition.
-   In the PAR Dashboard Permission \[par\_dashboard\_permission\] table, make sure the dashboard has at least one **User**, **Group**, or **Role** field populated.

Role required: sn\_spm\_ewd.ewd\_admin

## About this task

You can map a dashboard when you create a partition or later from an existing partition. Dashboard mappings are stored in the Partition Dashboard \[sn\_spm\_ewd\_partition\_dashboard\] table. You can map one dashboard to a partition for each experience.

In Strategic Planning Workspace, users select a partition from the **Current view** list on the Demands page. When a partition is selected, the **Dashboard** tab displays the dashboard mapped to that partition, and the **List** tab shows only the demands in that partition. The **Current view** list includes only the partitions that the user has access to.

## Procedure

1.  Navigate to **All** &gt; **Enterprise-Wide Deployment** &gt; **Partitions**.

2.  Select the partition that you want to map a dashboard to.

    For example, select **HR**.

3.  Select the **Partition Dashboards** tab.

4.  Select **New**.

    The Partition Dashboard form opens with the **Partition** field set to the current partition. The **Partition** field is read-only.

5.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Experience|Experience that the dashboard applies to, such as **Demand Management**.|
    |Dashboard|Dashboard to map to the partition for the selected experience.|

6.  Select **Submit**.

    The dashboard appears in the **Partition Dashboards** list for the partition. If a dashboard is already mapped to the partition for the same experience, the mapping isn't saved and an error message appears.


