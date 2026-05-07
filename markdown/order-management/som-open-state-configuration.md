---
title: Use extension points for open state management
description: Control the options displayed in the product configurator by using extension points in Open state management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy product configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
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
|OpenStateModelExtension|Method used to return to the updated config instance. Customers can customize the process method.|

