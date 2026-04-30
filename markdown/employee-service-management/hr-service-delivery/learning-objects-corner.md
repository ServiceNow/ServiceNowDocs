---
title: Learning objects for HR Service Delivery Integration with Cornerstone OnDemand
description: View details of learning objects that are pulled from the Cornerstone OnDemand system to ServiceNow system. Learning objects help in navigating users to the correct learning to-do details.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference for HR Service Delivery Integration with Cornerstone OnDemand, HR Service Delivery Integration with Cornerstone OnDemand, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Learning objects for HR Service Delivery Integration with Cornerstone OnDemand

View details of learning objects that are pulled from the Cornerstone OnDemand system to ServiceNow system. Learning objects help in navigating users to the correct learning to-do details.

When the Trigger CSOD Sync schedule flow is run, the flow in the Sync Trainings service pulls learning objects from the Cornerstone OnDemand system into the CSOD Learning Object Staging \[sn\_hr\_cornerstone\_lo\_staging\] table. After the transformation scripts are run, learning objects are displayed in**HR Cornerstone Integrations** &gt; **Learning Objects**.

|Field|Description|
|-----|-----------|
|Title|Name of the learning object.|
|Active|Option indicating that the learning object is in use.|
|Learning ID|Unique identifier of the learning object.|
|Learning Type|Type of learning object.|
|Learning Type ID|Unique identifier of the learning type.|
|Root LO|Parent of the learning object.|

**Note:**

-   These type of learning objects are not displayed in the Learning Objects page: Session, Cohort, Program, and Library type. These type of learning objects appear in the CSOD Learning Object Staging \[sn\_hr\_cornerstone\_lo\_staging\] table, but do not appear in the Learning Objects page after transformation.
-   Only the child topics of a certification are displayed as tasks in the To-dos page in Employee Center, and not the certification itself.


**Parent Topic:**[Reference for HR Service Delivery Integration with Cornerstone OnDemand](../reference/reference-ondemand.md)

**Related topics**  


[Components installed with HR Service Delivery Integration with Cornerstone OnDemand](../reference/installed-with-hr-corn-int.md)

[Source for HR Service Delivery Integration with Cornerstone OnDemand](hr-cornerstone-properties.md)

[HR Integration Services for HR Service Delivery Integration with Cornerstone OnDemand](cornerstone-hr-service.md)

[Users for HR Service Delivery Integration with Cornerstone OnDemand](users-cornerstone.md)

[Status mapping in Cornerstone OnDemand System](status-cornerstone.md)

[Transform maps for HR Service Delivery Integration with Cornerstone OnDemand](../reference/transform-maps-cornerstone.md)

