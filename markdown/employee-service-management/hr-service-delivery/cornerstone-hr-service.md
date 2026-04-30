---
title: HR Integration Services for HR Service Delivery Integration with Cornerstone OnDemand
description: Once you set up the HR Service Delivery Integration with Cornerstone OnDemand application, HR integration services for Cornerstone are automatically created in Enterprise Service Management Integrations Framework. The flows in HR Integration Services communicate with the Cornerstone OnDemand system to pull users, learning objects, and transcripts into ServiceNow.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, HR Service Delivery Integration with Cornerstone OnDemand, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# HR Integration Services for HR Service Delivery Integration with Cornerstone OnDemand

Once you set up the HR Service Delivery Integration with Cornerstone OnDemand application, HR integration services for Cornerstone are automatically created in Enterprise Service Management Integrations Framework. The flows in HR Integration Services communicate with the Cornerstone OnDemand system to pull users, learning objects, and transcripts into ServiceNow.

**Important:** You must activate all of these HR integration services so that data is properly synchronized between the Cornerstone OnDemand system and ServiceNow.

|Name|Description|
|----|-----------|
|Sync Users|This HR integration service maps users in the Cornerstone OnDemand system to users in the ServiceNow system using email Ids. When the Trigger CSOD Sync schedule flow is run, users are pulled from the Cornerstone OnDemand system to the User Mapping Staging \[sn\_hr\_cornerstone\_user\_mapping\_staging\] table. After transformation scripts are run, mapped users are displayed in **HR Cornerstone Integrations** &gt; **Users**.|
|Sync Trainings|This HR integration service pulls learning objects such videos or curriculum from the Cornerstone OnDemand system to the ServiceNow system. When the Trigger CSOD Sync schedule flow is run, learning objects are pulled into the CSOD Learning Object Staging \[sn\_hr\_cornerstone\_lo\_staging\] table. After the transformation scripts are run, learning objects are displayed in **HR Cornerstone Integrations** &gt; **Learning Objects**.|
|Sync Transcripts|This HR integration service pulls transcripts from the Cornerstone OnDemand system to the ServiceNow system. When the Trigger CSOD Sync schedule flow is run, transcripts are pulled into HR Pulled To-do Integration Staging \[sn\_hr\_integr\_fw\_todo\_inbound\_staging\] table. After the transformation scripts are run, transcripts are displayed in **HR Integrations Framework** &gt; **Todos**.|

**Parent Topic:**[Reference for HR Service Delivery Integration with Cornerstone OnDemand](../reference/reference-ondemand.md)

**Related topics**  


[Components installed with HR Service Delivery Integration with Cornerstone OnDemand](../reference/installed-with-hr-corn-int.md)

[Source for HR Service Delivery Integration with Cornerstone OnDemand](hr-cornerstone-properties.md)

[Users for HR Service Delivery Integration with Cornerstone OnDemand](users-cornerstone.md)

[Learning objects for HR Service Delivery Integration with Cornerstone OnDemand](learning-objects-corner.md)

[Status mapping in Cornerstone OnDemand System](status-cornerstone.md)

[Transform maps for HR Service Delivery Integration with Cornerstone OnDemand](../reference/transform-maps-cornerstone.md)

