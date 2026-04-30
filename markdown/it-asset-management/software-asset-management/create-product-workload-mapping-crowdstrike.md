---
title: Create a product workload mapping for CrowdStrike products
description: Create a product workload mapping for your CrowdStrike products for accurately associating specific products with the types of workloads they manage.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-01-22"
reading_time_minutes: 2
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create a product workload mapping for CrowdStrike products

Create a product workload mapping for your CrowdStrike products for accurately associating specific products with the types of workloads they manage.

## Before you begin

You must create a CrowdStrike integration profile before creating a workload mapping. For more information, see [Integrating with CrowdStrike](../concept/integrate-with-crowdstrike.md#).

Role required: sam\_admin or sam\_integrator

## About this task

Workload mapping is essential for accurately associating specific products with the types of workloads they manage. For example, servers, desktops, and containers. This is because CrowdStrike provides consumption data for endpoints or workloads instead of consumption data for specific products. Workload mapping enables you to map workloads that are consumed against each product. Based on the workload mapping that you create, the consumption across workloads is aggregated for each product, preventing over- or under-counting. This new approach replaces previous methods and aligns with how CrowdStrike now tracks usage, ensuring accurate compliance.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **User subscription** &gt; **CrowdStrike product workload mappings**.

2.  Select **New**.

3.  On the CrowdStrike Product Workload Mapping form, fill in the fields.

<table id="table_mdk_b33_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration profile

</td><td>

The integration profile for which the workload mapping is being created.This field is automatically populated when you navigate to the product workload mapping form from a particular integration profile.

</td></tr><tr><td>

Workload

</td><td>

Endpoints are physical or virtual devices, such as a computer, server, laptop, desktop computer, mobile, cellular, container, pod, or virtual machine image.Endpoints are sometimes referred to as workloads.

For example,

-   containers
-   public\_cloud\_with\_containers
-   servers\_without\_containers
-   chrome\_os


</td></tr><tr><td>

Software model

</td><td>

Profile of the software, which includes publisher, version, and discovery map.

</td></tr><tr><td>

License metric

</td><td>

License metric for the selected software model.-   **Reserved Hourly Average Sensor**: This metric counts the number of unique active endpoints per clock-hour and averages them over a rolling 28-day period. The count of Reserved Hourly Average Sensor Licenses resets at the start of each clock-hour.
-   **Sensor Subscription**: This metric calculates license usage by averaging endpoint counts over four consecutive weeks. Weekly endpoint counts are based on the total number of endpoints consumed in the previous seven days.


</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The mapping that you have created appears in the CrowdStrike product workload mapping list.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

**Related topics**  


[Integrating with CrowdStrike](../concept/integrate-with-crowdstrike.md#)

