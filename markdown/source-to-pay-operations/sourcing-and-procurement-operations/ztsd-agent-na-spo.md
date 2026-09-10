---
title: AI L1 SPO Service Desk Specialist
description: The AI L1 SPO Service Desk Specialist processes general inquiry procurement cases by searching knowledge resources and delivering resolutions with high confidence, reducing manual case handling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/ztsd-agent-na-spo.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 4
keywords: [Zero Touch Service Desk, ZTSD, AI L1 SPO Service Desk Specialist]
breadcrumb: [Use ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# AI L1 SPO Service Desk Specialist

The AI L1 SPO Service Desk Specialist processes general inquiry procurement cases by searching knowledge resources and delivering resolutions with high confidence, reducing manual case handling.

When a requester submits a general inquiry case, the AI L1 SPO Service Desk Specialist investigates the issue. It retrieves relevant information from published knowledge base articles and the FSC Common knowledge graph. If the agent determines that the case can be resolved with sufficient confidence, it posts the resolution in the **Activity** section and closes the case. If not, it assigns the case to Procurement Service Management assignment group, and routes it to a fulfiller for review.

## Plugins

To use the AI L1 SPO Service Desk Specialist, install the following plugins:

-   ServiceNow Otto for Sourcing and Procurement Operations \(`com.snc.sn_spend_gen_ai`\)
-   Zero Touch Service Desk \(`com.snc.sn_ztsd`\)

## Automated case resolution workflow

The AI L1 SPO Service Desk Specialist processes a general inquiry procurement case in the following steps.

1.  A requester submits a general inquiry through Employee Center or an email.
2.  Assignment rules route the case to the AI L1 SPO Service Desk Specialist.
3.  The agent retrieves case information and determines the inquiry context.
4.  The agent searches published knowledge base articles and the FSC Common knowledge graph for relevant guidance. For more information about knowledge graphs, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph-landing.md).
5.  The agent provides a resolution with helpful reference links in the **Resolution Notes** section. This gives the requester quick access to supporting documentation.
6.  The agent routes the case based on confidence scoring:
    -   Score greater or equal to 4: The case state changes to **Awaiting Acceptance**. The resolution is sent to the requester for acceptance and the case switches to read-only mode.
    -   Score less than 3: The case state changes to **Draft**. The agent assigns the case to the Procurement Service Management assignment group for fulfiller review.
7.  The requester receives the resolution by email and can access it in **My Tasks** in Employee Center or in the **To-Do** tab of the inquiry case.


## Case resolution outcomes

The outcome of the resolution process depends on the requester's response and Advanced Work Assignment configuration:

-   Accepted by requester: The case closes and is marked as **Closed Completed**.
-   Confidence score below 3 with Advanced Work Assignment active: The case state changes to **Draft** and routes to the Advanced Work Assignment queue for fulfiller review.
-   Rejected with Advanced Work Assignment active: The case state changes to **Draft** and moves to the Advanced Work Assignment queue. For more information on Advanced Work Assignment, see [Advanced Work Assignment for Source-to-Pay Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/awa-spo.md).
-   Rejected with Advanced Work Assignment inactive: The case state changes to **Draft**, and is unassigned from the agent.
-   No response within 72 hours: A scheduled job closes the case as **Closed Completed**.

-   **[View AI L1 SPO Service Desk Specialist progress](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/view-ztsd-na-spo.md)**  
Track the steps the AI L1 SPO Service Desk Specialist performs when processing a procurement case.
-   **[Edit Knowledge Graph tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/edit-kg-tags-spo.md)**  
Customize the instructions that the AI L1 SPO Service Desk Specialist uses to retrieve information by editing FSC Common Knowledge Graph tags.

**Parent Topic:**[Use ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-using.md)

**Related topics**  


[Summarize a procurement record in Source-to-Pay Workspace]()

[Summarize a procurement record in Shopping Hub]()

[Request the generative AI capabilites in ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) by using ServiceNow Otto panel]()

[Use ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) in Virtual Agent]()

[Generate an email response for procurement cases]()

[Analyze sentiment in procurement cases]()

[Generate a knowledge article]()

