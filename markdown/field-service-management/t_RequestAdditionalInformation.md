---
title: Request additional information to qualify a work order
description: Transfer orders move necessary parts to the location where the agent can receive them. If there is not enough information to create a transfer order, the dispatcher can request more details from the qualifier.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/field-service-management/t\_RequestAdditionalInformation.html
release: xanadu
product: Field Service Management
classification: field-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Qualifying work orders, Managing work orders, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Request additional information to qualify a work order

Transfer orders move necessary parts to the location where the agent can receive them. If there is not enough information to create a transfer order, the dispatcher can request more details from the qualifier.

## Before you begin

Role required: wm\_dispatcher or wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatch Queue**.

2.  Open a work order task in **Pending Dispatch** state.

3.  In the **Work Notes** field, enter a reason for returning the work order.

4.  Click **Request more information**.

    The task state changes to **Draft** and the work order state changes to **Awaiting Qualification**. If Field Service Management is configured for [automatic qualification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/c_QualifyWorkOrders.md), the work order state remains at **Qualified**.


**Parent Topic:**[Qualifying work orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/c_QualifyWorkOrders.md)

