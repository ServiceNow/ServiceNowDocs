---
title: Domain separation and Advanced Work Assignment
description: Domain separation is supported in the Advanced Work Assignment feature. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Domain separation and Advanced Work Assignment

Domain separation is supported in the Advanced Work Assignment feature. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see Application support for domain separation.

## Overview

Advanced Work Assignment enables the automatic assignment of work items to qualified agents using work item queues defined for specific service channels. Managed Service Providers can create domain-specific queues by specifying a particular domain as a queue routing condition.

## How domain separation works in Advanced Work Assignment

When an instance has a domain hierarchy where users and groups belong to different domains, you may need to restrict the visibility of work items to certain agents in a domain. You may also need to ensure that work items are routed to agents in the proper domain. AWA admins can configure service channels and associated work item queues to:

-   **Route work by domains**

    To push work items to agents in domains where only certain tasks or interactions are visible to them, use a routing condition that routes those items to the appropriate queues. For example:

    -   To restrict a queue to only items that match exactly to a particular domain X, specify this condition: **\[Domain\] \[is\] \[X\]**
    -   To route all work items in domain X and its child domains to a queue, use the **Domain Path** field and specify a condition such as: **\[Domain Path\] \[starts with\] \[!!!/!!\#/\]**
-   **Assign work to agents in the appropriate domain**

    To assign work items to agents in the appropriate domain, ensure that the assignment groups specified in the queue [Eligibility Assignment pools](../task/awa-specify-assignment-eligibility.md) have agents that belong to the domains where they can see the work items routed to the queue.

    If a mismatch occurs, and agents in an eligible assignment group cannot see a work item in a queue, AWA may temporarily assign an item to an agent. However, before the item is moved to the agent's inbox, AWA automatically rejects the assignment with the reason **No access**. AWA reassigns the work item to a different agent who might have access. If none of the available agents can see the work item, the item could be rejected multiple times.

    **Warning:** The item can get stuck in the queue until the AWA admin corrects the eligible assignment configuration.


**Related topics**  


[bundle-psec.domain-sep-landing-page]

