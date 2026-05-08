---
title: Universal Request
description: The Universal Request feature enables supplier contacts to raise issues that do not fit into predefined case types or involve multiple departments. It provides a structured workflow for routing and resolution of queries.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Universal Request

The Universal Request feature enables supplier contacts to raise issues that do not fit into predefined case types or involve multiple departments. It provides a structured workflow for routing and resolution of queries.

You must install the Universal Request for Source-to-Pay Operations plugin \[sn\_fsc\_ur\_common\] to enable the Universal Request feature in SLO. For more information on installing the plugin, see [Install Universal Request for SLO](../task/install-universal-request.md).

## Key Stakeholders

The Universal Request workflow involves the following stakeholders:

-   Supplier contacts: Supplier contacts submit their queries by raising Universal requests.
-   Routing agents: Routing agents are tier-1 agents who manage both Universal requests and supplier cases. These agents have both the Universal Request role and the \[sn\_slm.agent\] role. Routing agents can perform the following operations:
    -   View, update, transfer, and close Universal requests
    -   Create supplier cases from Universal requests

**Note:** You can create Routing agents by adding users to the Source Operations Universal Request Group. This group is a default assignment group that contains Universal request roles and supplier agent roles. For more information on assigning roles, see Assign roles to UR users.

For more information on roles in Universal requests, see Universal Request roles and groups.

## Universal Request workflow

1.  Submission of a Universal request

    The supplier contact submits a Universal request from the Supplier Collaboration portal. For more information on raising a Universal request, see [Create a Universal Request from the Supplier Collaboration Portal](create-universal-request.md).

2.  Assignment of the Universal request
    -   For requests that are marked as sensitive, suppliers select the department at the time of request submission. The request is assigned automatically to the corresponding assignment group.

        **Note:** Suppliers can mark a Universal request as sensitive by selecting the **Issue contains sensitive or confidential information** check box while submitting the request form. For more information, see [Create a Universal Request from the Supplier Collaboration Portal](create-universal-request.md).

    -   For requests that aren’t marked as sensitive, routing agents review the request and route them to an appropriate assignment group based on the information provided in the description and short description by the supplier.
3.  Primary ticket creation
    -   For requests that are marked as sensitive, a primary ticket of the type supplier case is created automatically.
    -   For requests that aren’t marked as sensitive, routing agents must create a supplier case for resolution. For more information, see [Create supplier case from Universal Request](../task/create-supplier-case.md).

        **Note:** Routing agents can also create an invoice case instead of a supplier case from a Universal request if they have the required permissions.

4.  Resolution of the Universal request
    -   If the routing agent accepts the resolution provided in the primary ticket, the Universal request is marked as complete and closed.
    -   If the resolution is rejected, the supplier case is dissociated from the Universal request. The routing agent then creates a new primary ticket from the Universal request for resolution.

Primary tickets can also be transferred to other departments when resolving a Universal request requires cross-departmental support or must be reassigned to a different department. For more information on transferring primary tickets, see Transfer a primary ticket.

When a Universal request needs support from multiple departments, you can create Associated tickets in addition to the primary ticket. Associated tickets enable multiple departments to work on the resolution of the Universal request simultaneously. For more information see, Create associated ticket for primary ticket of UR.

