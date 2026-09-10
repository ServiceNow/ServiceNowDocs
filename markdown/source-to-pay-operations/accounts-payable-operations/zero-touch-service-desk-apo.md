---
title: AI L1 APO Service Desk Specialist
description: The AI L1 APO Service Desk Specialist enables AI L1 Service Desk automation for invoice inquiry use cases through a flexible, agentic AI architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/zero-touch-service-desk-apo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-06-13"
reading_time_minutes: 2
keywords: [Zero Touch Service Desk, ZTSD, L1 service desk automation, agentic AI architecture, APO, Service Desk Specialist, FSC Common KG Tags, Supplier Collaboration Portal]
breadcrumb: [Use AI agents in ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# AI L1 APO Service Desk Specialist

The AI L1 APO Service Desk Specialist enables AI L1 Service Desk automation for invoice inquiry use cases through a flexible, agentic AI architecture.

## AI L1 APO Service Desk Specialist overview

The AI L1 APO Service Desk Specialist retrieves relevant information from published knowledge base articles and the FSC Common KG Tags added under the Enterprise knowledge graph to investigate the issue. If the specialist determines that the case can be resolved, it posts the resolution in the Activity section and closes the case. If the specialist can't resolve the case with sufficient confidence, it reassigns the case to a fallback assignment group for human follow-up.

## AI L1 APO Service Desk Specialist workflow

The following steps describe how the AI L1 APO Service Desk Specialist processes a general inquiry case.

-   **1. Supplier contact raises a general invoice inquiry case**

    The supplier contact submits a general inquiry through the Supplier Collaboration Portal or by sending an email. For more information on submitting supplier inquiries, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supp-catalog-req.md)

-   **2. Case assigned to the AI L1 APO Service Desk Specialist**

    An assignment rule automatically assigns the case to the AI L1 APO Service Desk Specialist.

-   **3. Fetch case details**

    The agent retrieves the case information to understand the context of the inquiry.

-   **4. Query knowledge sources**

    The agent searches published knowledge base articles and the FSC Common KG Tags knowledge graph for relevant guidance, such as invoice submission guidelines. To know more about Knowledge graphs, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph-landing.md).

-   **5. Generate a resolution**

    The agent composes a resolution based on its research and adds it to the **Activity** of the invoice inquiry case. The same resolution appears in the **Closed Notes**. This resolution is visible to the supplier contact on the Supplier Collaboration Portal.

-   **6. Evaluate confidence and update case state**

    The agent evaluates a confidence score for the resolution and updates the case state based on the configured threshold. The default threshold value is 70.

    -   If the confidence score exceeds the threshold, the case state changes to **Awaiting Acceptance** and the resolution is sent to the supplier contact for acceptance.
    -   If the confidence score does not exceed the threshold, the case is reassigned to the fallback assignment group for human follow-up. The default assignment group is AP Supplier Services.
-   **7. Resolution acceptance or rejection by the supplier contact**

    The supplier contact receives the resolution by email and can also view it under My Tasks on the Supplier Collaboration Portal.

    -   If the supplier contact accepts the resolution, the case is closed and marked as closed complete.
    -   If the supplier contact rejects the resolution, the case is updated with their comments and the supplier case is escalated to AP Supplier Services group for further investigation.
    -   If the supplier contact does not respond within 72 hours, a scheduled job runs daily to identify such cases and close them as closed complete. For more information on the supplier tasks in Supplier Collaboration Portal, see [AI worker case resolution confirmation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/ai-worker-case-resolution-confirmation.md).

**Related topics**  


[AI worker case resolution confirmation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/ai-worker-case-resolution-confirmation.md)

