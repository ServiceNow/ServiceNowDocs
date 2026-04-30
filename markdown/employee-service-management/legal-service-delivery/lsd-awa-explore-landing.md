---
title: Explore Advanced Work Assignment for Legal Service Delivery
description: Use the ServiceNow Advanced Work Assignment for Legal Service Delivery feature to automatically assign legal to agents based on availability, capacity, and optionally skills.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Advanced work assignment for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Explore Advanced Work Assignment for Legal Service Delivery

Use the ServiceNow Advanced Work Assignment for Legal Service Delivery feature to automatically assign legal to agents based on availability, capacity, and optionally skills.

## Advanced Work Assignment for Legal Service Delivery overview

Advanced Work Assignment for Legal Service Delivery routes legal request to qualified agents from the legal department \(a paralegal staff or lawyer\) using work item queues, routing conditions, and assignment criteria that you define. The base system has configuration available for General Legal Request and Ethics Complaint. You can define your own configuration for other types of legal requests.

For more information, see [Exploring Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

If you want to use skills as one of the criteria for routing legal requests, ensure you have activated Skills Management \[com.snc.skills\_management\]. For more information, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

**Note:** If you're using skill management, ensure you have the right subscription.

## Advanced Work Assignment for Legal Service Delivery workflow

1.  The legal Advanced Work Assignment administrator configures Advanced Work Assignment for Legal Service Delivery.
2.  A new legal request is submitted
3.  Advanced Work Assignment for Legal Service Delivery workflow identifies the new request to the available agents based on the availability, capacity and skills.
4.  The legal fulfiller accepts or rejects the work assignment.
    1.  The legal fulfiller accepts the assignment and works on it.
    2.  The legal fulfiller rejects the assignment. The legal request is reassigned to another agent as per the availability, capacity and skills.

## Advanced Work Assignment for Legal Service Delivery benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Automatic assignment of legal request based on availability, capacity and skills.|Advanced Work Assignment|Legal fulfiller|

For more information on the benefits of Advanced Work Assignment, see [Exploring Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

## What to explore next

To learn more about configuring and using Advanced Work Assignment for Legal Service Delivery, see:

-   [Configure Advanced Work Assignment for Legal Service Delivery](lsd-awa-configure-landing.md)
-   [Use Advanced Work Assignment for Legal Service Delivery](lsd-awa-use-landing.md)
-   [Components installed for Advanced Work Assignment for Legal Service Delivery reference](../reference/lsd-components-installed-awa.md)

**Parent Topic:**[Advanced work assignment for Legal Service Delivery](lsd-awa-landing.md)

