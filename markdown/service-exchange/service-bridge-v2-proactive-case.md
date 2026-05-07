---
title: Proactive cases
description: Proactively notifies consumer users of case alerts and enables real-time collaboration with providers without any additional configuration in connected consumer instances.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Service Exchange]
---

# Proactive cases

Proactively notifies consumer users of case alerts and enables real-time collaboration with providers without any additional configuration in connected consumer instances.

A proactive case in Service Exchange is similar to the synchronization that occurs between a provider's and customer's instances when the customer submits a service request. However, in this case, the fulfillment process proactively triggers by alert monitoring.

After a customer on boards through Service Exchange, that customer gets notified of cases that are created from alert monitoring. Customers proactively receive up-to-date information about issues that affect them, and are informed about the progress of the resolution of those issues.

The process is as follows:

1.  An alert that is related to an on boarded Service Exchange customer triggers in the provider's instance, and a case record is created.
2.  A link to the provider task is added as a comment in that case.
3.  An automatic Customer Service Management notification is sent to the primary customer contact, and a link to the provider task is also included.
4.  Any state changes or additional comments that are added to the case record in the provider's instance appear in the customer's instance. The status change in the case triggers creation of a case on the provider's instance.

For more information about the Service Exchange synchronization for resolving cases, see [Fulfill a consumer request](service-bridge-v2-proactive-customer-care-csp.md).

