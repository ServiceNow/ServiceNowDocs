---
title: AI L1 SLO Service Desk Specialist
description: The AI L1 SLO Service Desk Specialist is a fully autonomous help desk automation solution that resolves supplier inquiries without manual intervention from a fulfiller.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/ztsd-agent-slo.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 3
keywords: [AI L1 SLO Service Desk Specialist, general inquiry, supplier lifecycle operations, case resolution]
breadcrumb: [Use, ServiceNow Otto for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# AI L1 SLO Service Desk Specialist

The AI L1 SLO Service Desk Specialist is a fully autonomous help desk automation solution that resolves supplier inquiries without manual intervention from a fulfiller.

## AI L1 SLO Service Desk Specialist overview

When a supplier contact submits a general inquiry case, the AI L1 SLO Service Desk Specialist retrieves relevant information from published knowledge base articles and the FSC Common KG Tags added under the Enterprise knowledge graph to investigate the issue. If the specialist determines that the case can be resolved, it posts the resolution in the Activity section and closes the case. If the specialist cannot resolve the case with sufficient confidence, it reassigns the case to a fallback assignment group for human follow-up.

**Note:** By default, the AI L1 SLO Service Desk Specialist resolves only the general inquiry case type.

## Prerequisites

To access the AI L1 SLO Service Desk Specialist, you must have the following plugins installed:

-   ServiceNow Otto for SLO plugin \(com.snc.sn\_supplier\_gen\_ai\)
-   Zero Touch Service Desk plugin \(com.snc.sn\_ztsd\)

## AI L1 SLO Service Desk Specialist workflow

The following steps describe how the AI L1 SLO Service Desk Specialist processes a general inquiry case.

1.  **Supplier contact raises a general inquiry case**: The supplier contact submits a general inquiry through the Supplier Collaboration Portal or by sending an email. For more information on submitting supplier inquiries, see [Raising requests from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supp-catalog-req.md).
2.  **Case assigned to the AI L1 SLO Service Desk Specialist**: An assignment rule automatically assigns the case to the AI L1 SLO Service Desk Specialist.
3.  **Fetch case details**: The agent retrieves the case information to evaluate the context of the inquiry.
4.  **Query knowledge sources**: The agent searches published knowledge base articles and the FSC Common KG Tags knowledge graph for relevant guidance, such as supplier onboarding guidelines. For more information on knowledge graphs, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph-landing.md).
5.  **Generate a resolution**: The agent provides a resolution and lists helpful reference links in the **Resolution Notes** section. This gives the requester quick access to related documentation and solutions that support the resolution. This resolution is visible to the supplier contact on the Supplier Collaboration Portal.
6.  **Evaluate confidence and update case state**:

    The agent acts based on the confidence score of the search results:

    -   Score above 70%: The case state changes to **Awaiting Acceptance**. The resolution is sent to the requester for acceptance and the case switches to read-only mode.
    -   Score at or below 70%: The agent sets the request state to **Draft** and the case is reassigned to the fallback assignment group for human follow-up. The default assignment group is Supplier Administrators.
7.  **Resolution acceptance or rejection by the supplier contact**:

    The supplier contact receives the resolution by email and can also view it under **My Tasks** on the Supplier Collaboration Portal.

    -   If the supplier contact accepts the resolution, the case is closed and marked as **Closed Complete**.
    -   If the supplier contact rejects the resolution, the case status changes to **Work in Progress** and the supplier case is escalated to a support engineer for human follow-up.
    -   If the supplier contact does not respond within 72 hours, a scheduled job runs daily to identify such cases and close them as closed complete.

## Escalation to a human agent

The AI L1 SLO Service Desk Specialist automatically escalates a case and returns it to a draft state in the following scenarios:

-   The agent does not identify a resolution for the contact's question.
-   The number of exchanges between the agent and the supplier contact exceeds the configured limit.

