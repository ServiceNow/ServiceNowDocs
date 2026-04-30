---
title: Domain separation and Strategic Planning
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Strategic Planning. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Domain separation and Strategic Planning

Domain separation is supported for Strategic Planning. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Overview of domain separation in Strategic Planning

You can create lens, portfolio plans, planning items, and roadmaps in different domains.

## How domain separation works in Strategic Planning

After you enable domain separation on your ServiceNow instance, the data of Strategic Planning is automatically domain separated. So, the data of lens, portfolio plans, planning items, and roadmap configuration for different domains is visible to only those users who have access to these domains.

## Domain separated tables in Strategic Planning

All the tables installed with Strategic Planning support domain separation. For a complete list of tables, see [Components installed with Strategic Planning Workspace](../reference/components-installed-with-alignment-planner-workspace.md).

**Parent Topic:**[Strategic Planning Workspace reference](../reference/alignment-planner-workspace-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

