---
title: Explore HR Service Delivery Integration with Magnit
description: Understand the end-to-end work flow of HR Service Delivery Integration with Magnit.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Integration with Magnit, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Explore HR Service Delivery Integration with Magnit

Understand the end-to-end work flow of HR Service Delivery Integration with Magnit.

## End-to-end flow

1.  Ensure that the manager profile is available in the ServiceNow AI Platform instance before pulling contingent worker information.
2.  Import ​Location, Department, Job that must be associated to the contingent worker into ServiceNow AI Platform instance \(for example, via bulk import\). In case, you do not import the corresponding IDs, these values remain null for the contingent employee​.
3.  With the sn\_hr\_magnit.admin role, create relevant HR task templates and associate them to onboarding items pulled from Magnit instance. For more information, see [Map Magnit tasks](../task/magnit-task-mapping.md).
4.  Create the following properties for the Magnit source. These are one-time configurations:​

    -   **full\_pull\_wait\_time**: Wait time between receiving correlation ID and calling the full pull action
    -   **delta\_pull\_wait\_time**: Wait time between receiving correlation ID and calling the delta pull action
    ​ For more information, see [Source for HR Service Delivery Integration with Magnit](../reference/source-magnit.md#).

5.  Pull contingent workers from Magnit application into ServiceNow AI Platform instance via a scheduled job that can be configured. See [Activate a schedule flow](../task/activate-sch-flow-magnit.md).

    A life cycle event is triggered and a lifecycle case is created for each contingent worker. An HR task is created for each onboarding item within the lifecycle case.

    **Note:** If an HR task is not created for onboarding item, verify if an active Magnit mapping record exists for that onboarding item. For more information, see [Map Magnit tasks](../task/magnit-task-mapping.md).​

    Contingent workers complete onboarding tasks from ServiceNow AI Platform instance.


![End-to-end work flow of HR Service Delivery Integration with Magnit.](../image/magnit-flow.png "Flow diagram")

