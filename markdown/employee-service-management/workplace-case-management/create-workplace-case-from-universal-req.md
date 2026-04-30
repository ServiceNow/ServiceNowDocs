---
title: Create a workplace case from Universal Request
description: As a routing agent, create a workplace case from a universal request and then assign it to the Workplace services assignment group. The workplace manager handles the workplace case and takes further actions to fulfill the request.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration with Universal Request, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a workplace case from Universal Request

As a routing agent, create a workplace case from a universal request and then assign it to the Workplace services assignment group. The workplace manager handles the workplace case and takes further actions to fulfill the request.

## Before you begin

Ensure that you have the following plugins installed:

-   Universal Request \(com.snc.universal\_request\)
-   Workplace Service Delivery - Core \(sn\_wsd\_core\)
-   Workplace Case Management \(sn\_wsd\_case\)

Role required: routing\_agent and sn\_wsd\_case.case\_writer

## Procedure

1.  Navigate to **Universal Requests** &gt; **All**.

2.  Open the universal request record from which you want to create a workplace case.

3.  Click **Create Workplace Case**.


## Result

A workplace case is created and is automatically assigned to the Workplace services assignment group. If required, you can also add more details on the Workplace Case form.

On the Workplace Case form, the universal request number that was used for creating the workplace case is displayed. The Workplace case number appears in the primary **Ticket** field on the Universal Request form and also under the Associated Tickets related list.

**Parent Topic:**[Workplace Service Delivery integration with Universal Request](../concept/wsd-intergration-with-universal-request.md)

**Related topics**  


[Configure a workplace service record producer as a Universal Request](configure-workplace-service-record-prod-as-universal-req.md)

[Work on a workplace case from a Universal Request](work-on-workplace-case-of-universal-req.md)

[Transfer a workplace case created from a universal request](transfer-a-workplace-case-created-from-a-universal-request.md)

