---
title: Source for HR Service Delivery Integration with Cornerstone OnDemand
description: Once you set up the HR Service Delivery Integration with Cornerstone OnDemand application, the source record for Cornerstone On Demand application is automatically created in Enterprise Service Management Integrations Framework, Source module. The Cornerstone OnDemand source record in the in Enterprise Service Management Integrations Framework application contains a predefined set of properties and HR Integration Services.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference for HR Service Delivery Integration with Cornerstone OnDemand, HR Service Delivery Integration with Cornerstone OnDemand, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Source for HR Service Delivery Integration with Cornerstone OnDemand

Once you set up the HR Service Delivery Integration with Cornerstone OnDemand application, the source record for Cornerstone On Demand application is automatically created in Enterprise Service Management Integrations Framework, Source module. The Cornerstone OnDemand source record in the in Enterprise Service Management Integrations Framework application contains a predefined set of properties and HR Integration Services.

<table id="table_tyz_xpj_1nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Full-pull

</td><td>

When set to **True**, all the active users, active trainings, incomplete to-dos from the Cornerstone OnDemand system are pulled into respective tables in ServiceNow instance.

 When set to **False**, only modified users, modified trainings, modified transcripts \(based on last successful schedule run time\) are pulled from the Cornerstone OnDemand system are pulled into respective tables in ServiceNow instance.

 **Note:** If there is no information on the last successful schedule run time, the first pull will always be a full pull.

</td></tr><tr><td>

page-count

</td><td>

Number of records that are pulled through an API call from the Cornerstone OnDemand system. By default, the value is **500**.**Note:** This property is honored only by the Sync Trainings and Sync Transcripts HR Integration Services, and not by Sync Users HR Integration Service.

</td></tr><tr><td>

url-prefix

</td><td>

Deep link prefix to pull learning objects from the Cornerstone OnDemand system during run time. For more information, see [Use deep link for HR Service Delivery Integration with Cornerstone OnDemand](../task/generate-deep-link-cor.md).

</td></tr></tbody>
</table>**Parent Topic:**[Reference for HR Service Delivery Integration with Cornerstone OnDemand](../reference/reference-ondemand.md)

**Related topics**  


[Components installed with HR Service Delivery Integration with Cornerstone OnDemand](../reference/installed-with-hr-corn-int.md)

[HR Integration Services for HR Service Delivery Integration with Cornerstone OnDemand](cornerstone-hr-service.md)

[Users for HR Service Delivery Integration with Cornerstone OnDemand](users-cornerstone.md)

[Learning objects for HR Service Delivery Integration with Cornerstone OnDemand](learning-objects-corner.md)

[Status mapping in Cornerstone OnDemand System](status-cornerstone.md)

[Transform maps for HR Service Delivery Integration with Cornerstone OnDemand](../reference/transform-maps-cornerstone.md)

