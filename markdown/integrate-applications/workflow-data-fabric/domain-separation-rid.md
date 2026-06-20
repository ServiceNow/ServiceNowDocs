---
title: Domain separation and Requirement Intake Diagram
description: Domain separation is supported for Requirement Intake Diagram. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/workflow-data-fabric/domain-separation-rid.html
release: zurich
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Requirement Intake Diagram reference, Requirement Intake Diagram, Workflow Data Fabric]
---

# Domain separation and Requirement Intake Diagram

Domain separation is supported for Requirement Intake Diagram. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Overview for Requirement Intake Diagram

The goal of Requirement Intake Diagram is to govern the end-to-end multi-vendor life cycle from one place. Domain separation is enabled in all the features.

You should have either a flat hierarchy or a single-tier hierarchy and at least one primary or top-level domain.

