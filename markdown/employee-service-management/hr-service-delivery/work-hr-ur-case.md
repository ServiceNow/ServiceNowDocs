---
title: Work on an HR case of Universal Request
description: Provide resolution to an HR case that is initiated from a universal request.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Universal Request for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Work on an HR case of Universal Request

Provide resolution to an HR case that is initiated from a universal request.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## About this task

The state changes described in the procedure can be configured to suit your requirements. For more information, see [Universal Request state mapping](../../universal-request/task/ur-state-mapping.md)

## Procedure

1.  Open the HR case that is created from a Universal Request.

2.  Click **Start Work**.

    The state of the case changes to **Work in Progress**.

    **Note:**

    -   If another department in HR must work on the request, you can transfer the case with the same number or with a new number. When you transfer the case with a new number, the universal request gets associated to that new case number.
    -   If this issue is not related to the HR department, the HR agent must select the **Transfer** option on the case. For more details on how to transfer the case, see [Transfer an HR case in Universal Request](route-ur-hr-case.md).
3.  Click **Closed Complete** when the resolution is provided.

    The state of the HR case is changed to **Awaiting acceptance** and the state of the universal request is automatically changed to **Awaiting response from user**. On the Employee Center:

    -   If the user accepts the resolution, the state of the universal request is changed to **Closed**. The state of the HR case is automatically changed to **Closed Complete**.
    -   If the user rejects the resolution, the state of the universal request is changed to **In progress**. The state of the HR case is automatically changed to **Work in progress.**
    **Important:** If for any reason the HR agent clicks **Closed Incomplete** without routing the HR case back to universal request, then the behavior is as follows:

    -   If the **Needs Additional Review** check box is selected on the universal request, the universal request will be in the **In progress** state, and the HR case will be in the **Close Incomplete** state.
    -   If the **Needs Additional Review** check box is deselected on the universal request, the universal request gets closed based on the state mapping.

**Parent Topic:**[Universal Request for HR Service Delivery](../concept/universal-request-hr.md)

