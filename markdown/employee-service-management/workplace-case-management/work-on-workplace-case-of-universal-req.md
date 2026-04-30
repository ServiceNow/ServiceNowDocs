---
title: Work on a workplace case from a Universal Request
description: As a workplace manager, work on a workplace case that is created from a Universal Request. Provide a resolution to the workplace case.
locale: en-US
release: yokohama
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workplace Service Delivery integration with Universal Request, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Work on a workplace case from a Universal Request

As a workplace manager, work on a workplace case that is created from a Universal Request. Provide a resolution to the workplace case.

## Before you begin

Role required: sn\_wsd\_case.case\_writer

## About this task

You can configure the state changes that are described in the following procedure as per your requirements. For more information, see [Universal Request state mapping](../../universal-request/task/ur-state-mapping.md).

## Procedure

1.  Navigate to **Workplace Case Management** &gt; **Workplace cases** &gt; **All**.

2.  Select the workplace case record that is created from the Universal Request.

3.  On the form, change the **State** field to **Work in progress**.

    **Note:** If the workplace case does not relate to any workplace service, then transfer the case to the relevant department or back to the Universal Request queue. Select **Transfer** to transfer the case. For more details on how to transfer a case, see [Transfer a workplace case created from a universal request](transfer-a-workplace-case-created-from-a-universal-request.md).

4.  When you resolve the case, change the state to **Closed complete**.


## Result

The state of the Universal Request is updated based on the state of the workplace case. For more information about state changes of a Universal Request, see [Universal Request states and reasons](../../universal-request/concept/ur-states.md).

If you change the state of the workplace case to Close incomplete without transferring the case back to the Universal Request queue or to another department, then one of the following actions is performed:

-   If the **Needs Additional Review** option is selected on the Universal Request, then the state of the request changes to the In progress state.
-   If the **Needs Additional Review** option is not selected on the Universal Request, then the request is closed based on the state mapping.

**Parent Topic:**[Workplace Service Delivery integration with Universal Request](../concept/wsd-intergration-with-universal-request.md)

**Related topics**  


[Configure a workplace service record producer as a Universal Request](configure-workplace-service-record-prod-as-universal-req.md)

[Create a workplace case from Universal Request](create-workplace-case-from-universal-req.md)

[Transfer a workplace case created from a universal request](transfer-a-workplace-case-created-from-a-universal-request.md)

