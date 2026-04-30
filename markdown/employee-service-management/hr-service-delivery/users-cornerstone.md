---
title: Users for HR Service Delivery Integration with Cornerstone OnDemand
description: Users from the Cornerstone OnDemand system are mapped to the users in ServiceNow system using email Ids. User mapping helps in assigning learning tasks to the correct user in the ServiceNow system.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference for HR Service Delivery Integration with Cornerstone OnDemand, HR Service Delivery Integration with Cornerstone OnDemand, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Users for HR Service Delivery Integration with Cornerstone OnDemand

Users from the Cornerstone OnDemand system are mapped to the users in ServiceNow system using email Ids. User mapping helps in assigning learning tasks to the correct user in the ServiceNow system.

When the Trigger CSOD Sync schedule flow is run, users are pulled from the Cornerstone OnDemand system to the User Mapping Staging \[sn\_hr\_cornerstone\_user\_mapping\_staging\] table. Once the transformation scripts are run, mapped users are displayed in **HR Cornerstone Integrations** &gt; **Users**.

|Field|Description|
|-----|-----------|
|CSOD ID|CSOD ID from Cornerstone OnDemand system.|
|Active|Option that indicates whether or not the user is active in the Cornerstone OnDemand system.|
|User|Name of the user in the ServiceNow system.|
|CSOD User|Name of the user in the Cornerstone OnDemand system.|
|CSOD User ID|ID of the user in the Cornerstone OnDemand system.|
|CSOD Email|Email ID of the user in the Cornerstone OnDemand system.|

**Note:** In case you want to use **CSOD ID**, **CSOD user**, and **CSOD User ID** fields for mapping users, you must override the getUser method in CSODIntegrationsUtil script.

**Parent Topic:**[Reference for HR Service Delivery Integration with Cornerstone OnDemand](../reference/reference-ondemand.md)

**Related topics**  


[Components installed with HR Service Delivery Integration with Cornerstone OnDemand](../reference/installed-with-hr-corn-int.md)

[Source for HR Service Delivery Integration with Cornerstone OnDemand](hr-cornerstone-properties.md)

[HR Integration Services for HR Service Delivery Integration with Cornerstone OnDemand](cornerstone-hr-service.md)

[Learning objects for HR Service Delivery Integration with Cornerstone OnDemand](learning-objects-corner.md)

[Status mapping in Cornerstone OnDemand System](status-cornerstone.md)

[Transform maps for HR Service Delivery Integration with Cornerstone OnDemand](../reference/transform-maps-cornerstone.md)

