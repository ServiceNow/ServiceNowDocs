---
title: Configure HR Service Delivery Integration with Magnit
description: Configure HR Service Delivery Integration with Magnit to create onboarding tasks for contingent workers.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Integration with Magnit, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure HR Service Delivery Integration with Magnit

Configure HR Service Delivery Integration with Magnit to create onboarding tasks for contingent workers.

## Before you begin

Role required: sn\_hr\_magnit.admin

Ensure that the manager profile is available in the ServiceNow AI Platform instance before pulling contingent worker information. Import ​Location, Department, Job that must be associated to the contingent worker into ServiceNow AI Platform instance \(for example, via bulk import\). In case, you do not import the corresponding IDs, these values remain null for the contingent employee​.

## Procedure

1.  [Map Magnit tasks](magnit-task-mapping.md) to create adhoc tasks for contingent workers.

2.  Configure properties in [Source for HR Service Delivery Integration with Magnit](../reference/source-magnit.md#).

3.  [Activate a schedule flow](activate-sch-flow-magnit.md) to pull contingent workers from Magnit application into ServiceNow AI Platform instance.

    A lifecycle event is triggered and a lifecycle case is created for each contingent worker. An HR task is created for each onboarding item within the lifecycle case.

    **Note:**

    -   If an HR task is not created for onboarding item, verify if an active Magnit mapping record exists for that onboarding item.
    -   If HR profile, lifecycle case or an HR task is not created for a onboarding item, verify if all Restricted caller access are in **Allowed** state.​

