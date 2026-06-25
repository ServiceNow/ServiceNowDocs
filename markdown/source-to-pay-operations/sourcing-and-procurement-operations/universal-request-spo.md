---
title: Universal Request in Sourcing and Procurement Operations
description: Universal Request \(UR\) in Sourcing and Procurement Operations enables employees to submit procurement-related requests through Employee Center, even when a request requires collaboration across multiple departments or teams. After submission, a routing agent creates a procurement case and routes it to the appropriate fulfillers for resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/universal-request-spo.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-06-12"
reading_time_minutes: 3
keywords: [Universal Request, universal request, ur, Universal Request in SPO, Universal Request in Sourcing and Procurement Operations]
breadcrumb: [Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Universal Request in Sourcing and Procurement Operations

Universal Request \(UR\) in Sourcing and Procurement Operations enables employees to submit procurement-related requests through Employee Center, even when a request requires collaboration across multiple departments or teams. After submission, a routing agent creates a procurement case and routes it to the appropriate fulfillers for resolution.

## Plugin

To enable Universal Request in Sourcing and Procurement Operations, install the Universal Request for Source-to-Pay Operations plugin \(sn\_fsc\_ur\_common\). For more information, see [Install Universal Request for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/install-universal-request-spo.md).

## Key stakeholders

-   Employees submit procurement-related requests by creating Universal Requests in Employee Center.
-   Routing agents are tier-1 agents who manage Universal Requests and procurement cases. Routing agents can view, update, transfer, and close Universal Requests, and create procurement cases from Universal Requests.

To create routing agents, add users to the Source Operations Universal Request Group. For more information, see [Universal Request roles and groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/ur-roles.md) and [Assign roles to UR users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/ur-assign-roles.md).

## Universal Request workflow

1.  An employee submits a Universal Request from Employee Center.

    For more information, see [Create a Universal Request from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-universal-request.md).

2.  A routing agent reviews the request and routes it to the appropriate team based on the short description and additional details provided.
3.  The routing agent creates a procurement case as the primary ticket for resolution.

    For more information, see [Create a procurement case from a Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/create-procurement-case-from-ur.md).

4.  When **Need resolution review** is enabled, the routing agent reviews the resolution and determines the next steps:

    -   Accepts the resolution: The Universal Request is marked as **Closed**.
    -   Rejects the resolution: The procurement case is dissociated from the Universal Request, and a new primary ticket is created for further resolution.

        **Note:** By default, **Need resolution review** is enabled.

    Status updates sync automatically to the Universal Request. The employee can track progress on the **Activity** tab in their Universal Request in Employee Center.


**Parent Topic:**[Explore Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/exploring-spo.md)

**Related topics**  


[Shopping Hub]()

[Shopping Hub Mobile]()

[Performance Analytics for Sourcing and Procurement Operations]()

[Sourcing and Purchasing Automation]()

[Procurement Case Management]()

[Source-to-Pay Workspace]()

[Spend and Savings Management]()

[Sourcing Pipeline Management]()

[Understanding Punchout]()

[AI Search for Sourcing and Procurement Operations]()

