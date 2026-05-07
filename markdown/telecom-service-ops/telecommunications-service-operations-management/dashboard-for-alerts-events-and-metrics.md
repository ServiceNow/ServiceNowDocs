---
title: SD-WAN Inventory Dashboard
description: The SD-WAN Inventory Dashboard provides a visual summary of your SD-WAN network inventory, including total customers, sites, devices, and models, with breakdowns by device model and class.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Performance management: Metric collection, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# SD-WAN Inventory Dashboard

The SD-WAN Inventory Dashboard provides a visual summary of your SD-WAN network inventory, including total customers, sites, devices, and models, with breakdowns by device model and class.

## Accessing the SD-WAN Inventory Dashboard

If you're a user with the tsom\_assurance\_admin role, you can access the SD-WAN Inventory Dashboard by navigating to **All** &gt; **Platform Analytics &gt; Dashboards** and searching for and selecting SD-WAN Inventory Dashboard.

![SD-WAN Inventory Dashboard: Network Overview tab](../images/Dashboard.png)

## Network Overview

The **Network Overview** tab provides a high-level summary of all discovered SD-WAN network inventory in the CMDB.

The following breakdowns are available in the SD-WAN Inventory Dashboard:

-   Total devices by model
-   Total devices by class

|Title|Type|Description|
|-----|----|-----------|
|Total customers|Single score|The total number of customers with SD-WAN network inventory discovered in the CMDB.|
|Total Sites|Single score|The total number of sites across all customers with discovered SD-WAN inventory.|
|Total Devices|Single score|The total number of SD-WAN devices discovered in the CMDB.|
|Total Models|Single score|The total number of distinct device models discovered across the SD-WAN network.|
|Total Devices by Model|Donut chart|The distribution of discovered devices by hardware model.|
|Total Devices by Class|Donut chart|The distribution of discovered devices by device class, such as IP Router, Wireless Access Point, and IP Camera.|

## Filtered View

The **Filtered View** tab provides the ability to filter inventory data by customer, manufacturer, model, or discovery source.

![SD-WAN Inventory Dashboard: Filtered View tab](../images/sd-wan-inventory-dashboard-fv.png)

|Title|Type|Description|
|-----|----|-----------|
|Customers|Single score|The number of customers matching the applied filter criteria.|
|Sites|Single score|The number of sites matching the applied filter criteria.|
|Sites by Customer|Bar Chart|The number of sites per customer matching the applied filter criteria.|
|Devices by Model|Donut Chart|The distribution of filtered devices by hardware model.|
|Devices by Class|Donut Chart|The distribution of filtered devices by device class.|

