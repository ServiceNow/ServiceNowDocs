---
title: Use extension points for open state management
description: Control the options displayed in the product configurator by using extension points in Open state management.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-04-09"
reading_time_minutes: 1
breadcrumb: [Setting up the product configurator, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Use extension points for open state management

Control the options displayed in the product configurator by using extension points in Open state management.

You can use extension points to call custom scripts for managing the product configurator.

As an admin, access the available open state management extension points, by navigating to **All** &gt; **Scripted Extension Points** and in the Extension Points list, select the appropriate extension point to view it.

|Extension points|Description|
|----------------|-----------|
|ConfigInstanceAPIImpl|Fetches open state execution for config instances during change and on load commands.|
|OpenStateValidation|Returns open state execution on config instances during change and on load.|
|SetOpenStateResponse|Updates the open state config instance to a config instance.|
|OpenStateModelExtension|Provides methods used to return to the updated config instance.|

## Using the OpenStateModelExtension point

When you install Configuration Rules Management, you can use the OpenStateModelExtension point and the canProcess\(\) method to set the custom logic to run either the configuration rules implementation or the open state implementation:

-   If you want to use open state rather than configuration rules, use the OpenStateModelExtension point and the canProcess\(\) method to return true for the open state implementation and turn off the configuration rules implementation.
-   If you're using open state but want to use configuration rules, use the OpenStateModelExtension point and the canProcess\(\) method to return true for the configuration rules implementation and turn off the open state implementation.

