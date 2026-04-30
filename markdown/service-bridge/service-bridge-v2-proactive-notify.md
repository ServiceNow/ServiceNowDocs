---
title: Proactive Service Exchange case notification in Service Exchange
description: After a customer onboards through Service Exchange, that customer gets notified of cases that are created from alert monitoring. Customers proactively receive up-to-date information about issues that affect them, and are informed about the progress of the resolution of those issues.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use for providers, Service Exchange for Providers, Service Exchange]
---

# Proactive Service Exchange case notification in Service Exchange

After a customer onboards through Service Exchange, that customer gets notified of cases that are created from alert monitoring. Customers proactively receive up-to-date information about issues that affect them, and are informed about the progress of the resolution of those issues.

A proactive case in Service Exchange is similar to the synchronization that occurs between a provider's and customer's instances when the customer submits a service request. However, in this case, the fulfillment process proactively triggers by alert monitoring.

The process is as follows:

1.  An alert that is related to an onboarded Service Exchange customer triggers in the provider's instance, and a case record is created.
2.  A link to the provider task is added as a comment in that case.
3.  An automatic Customer Service Management notification is sent to the primary customer contact, and a link to the provider task is also included.
4.  Any state changes or additional comments that are added to the case record in the provider's instance appear in the customer's instance. The status change in the case triggers creation of a case on the provider's instance.

For more information about the Service Exchange synchronization for resolving cases, see [Service Exchange Remote Catalog items](service-bridge-v2-proactive-customer-care-csp.md).

