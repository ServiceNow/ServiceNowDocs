---
title: Using HR Multi Instance Integration for Consumer
description: Access a remote catalog item \(hosted by a remote service provider\) and submit the catalog item with the required details from your Employee portal. An HR case is created in the provider instance which is fulfilled by a provider agent.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, HR Multi Instance Integration, HR Service Delivery, Employee Service Management]
---

# Using HR Multi Instance Integration for Consumer

Access a remote catalog item \(hosted by a remote service provider\) and submit the catalog item with the required details from your Employee portal. An HR case is created in the provider instance which is fulfilled by a provider agent.

## Before you begin

Role required: sn\_sb.requestor

## Procedure

1.  Navigate to the consumer employee portal.

2.  Select an HR catalog or catalog to place your request.

    This request triggers an approval flow \(not a required flow\) for your managerial approval. Once the HR request is approved by your manager, a provider task is created that in turn creates a remote HR case in provider instance.

    **Note:** You can access only the remote catalogs that have been enabled by your consumer administrator. See [Configure HR Multi Instance Integration for Consumer](../task/config-hr-multi-instance.md) for more information.

3.  Review if any tasks are assigned to you.

    **Note:** To fulfill your HR request, an HR agent from provider instance can request for any additional information from you or can create some additional tasks for you to complete.

4.  Select the URL link on the task that is assigned to you.

    Without having you to manually log in, the URL link gives you the access to linked resource in the provider instance for completing the task. After you complete the HR task in provider instance, your universal task is auto-closed in the consumer instance.

    Your HR request gets closed when the remote HR case is closed by the HR agent in provider instance.


