---
title: Source for HR Service Delivery Integration with Magnit
description: Once you set up the HR Service Delivery Integration with Magnit application, the source record for HR Service Delivery Integration with Magnit application is automatically created in Enterprise Service Management Integrations Framework, Source module. The Magnit source record in the Enterprise Service Management Integrations Framework application contains a predefined set of properties and HR integration service.Once you set up the HR Service Delivery Integration with Magnit application, HR integration service for Magnit is automatically created in Enterprise Service Management Integrations Framework. The flow in HR Integration Service communicates with the Magnit system to pull contingent workers into ServiceNow AI Platform instance.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery Integration with Magnit, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Source for HR Service Delivery Integration with Magnit

Once you set up the HR Service Delivery Integration with Magnit application, the source record for HR Service Delivery Integration with Magnit application is automatically created in Enterprise Service Management Integrations Framework, Source module. The Magnit source record in the Enterprise Service Management Integrations Framework application contains a predefined set of properties and HR integration service.

<table id="table_xsd_mpx_xvb"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

full\_pull\_wait\_time

</td><td>

Wait time between receiving correlation ID and calling the full pull action. **Note:** This property must be configured. It is a one time configuration.

</td></tr><tr><td>

delta\_pull\_wait\_time

</td><td>

Wait time between receiving correlation Id and calling the delta pull action.**Note:** This property must be configured. It is a one time configuration.

</td></tr><tr><td>

full pull

</td><td>

When set to **true**, active employees onboarded in Magnit are pulled to ServiceNow AI Platform instance along with its associated onboarding items. A lifecycle case is created for the each user along with adhoc tasks based on the onboarding items.When set to **false**, new employees onboarded in Magnit \(since the last successful pull\) are synchronized to ServiceNow AI Platform instance.​ Any change in the details of contingent worker in Magnit which are already present in ServiceNow AI Platform is synchronized to the ServiceNow AI Platform via a delta pull. If there are new onboarding items that got associated to the employee after the last pull, new HR tasks are created.

**Note:** If there is an active lifecycle case for a contingent worker, then new onboarding tasks are created within the same lifecycle case. If there is no active lifecycle case associated to the contingent worker, then a new lifecycle case is created for the employee and onboarding tasks are created within it.

 **Note:** full pull is an optional property.

</td></tr></tbody>
</table>## HR Integration Service for HR Service Delivery Integration with Magnit

Once you set up the HR Service Delivery Integration with Magnit application, HR integration service for Magnit is automatically created in Enterprise Service Management Integrations Framework. The flow in HR Integration Service communicates with the Magnit system to pull contingent workers into ServiceNow AI Platform instance.

|Name|Description|
|----|-----------|
|Get Contingent Worker|Pulls contingent workers from Magnit application into ServiceNow AI Platform instance.|

