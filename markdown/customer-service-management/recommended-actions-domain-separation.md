---
title: Domain separation and Recommended Actions
description: Domain separation is supported for Recommended Actions. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Domain separation and Recommended Actions

Domain separation is supported for Recommended Actions. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Overview

The tables and data in the application are domain separated. Recommendation authors can only see the context applicable to them based on the domain. In runtime, recommendations are evaluated in the user context and data is created in the corresponding domain applicable to the user.

## How domain separation works in Recommended Actions

To use domain separation in the Recommended Actions application, you can create separate Context records for each domain. Context serves as a starting point in Recommended Actions. All other configurations such as Rule, Recommendation, and Resource Generator can then be associated with the domain of the corresponding context record.

Runtime evaluation and generation of recommendations are user-specific. The user's domain is selected and the corresponding Rules applicable to the user are evaluated to give final recommendations to the end user. Execution records created use the same domain of the context that are applicable for the given user.

## Domain-separated tables

When you create related entities for a context, the domain for the related entities is set to the domain of the context. The following tables in the application are domain separated:

-   Context
-   Recommended Action Rule
-   Recommendation
-   Resource generator
-   Recommendation group
-   Search result recommended action mapping
-   Recommended Action Context
-   Recommended Action Execution
-   Recommended Action Order
-   Field recommendation
-   Field recommendation input
-   Field recommendation definition
-   Resource generator type
-   Resource generator type input
-   Recommendation grouping strategy
-   Action Type Definition
-   Trend Definition

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

