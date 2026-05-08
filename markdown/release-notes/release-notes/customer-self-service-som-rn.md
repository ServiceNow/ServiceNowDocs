---
title: Customer self-service for Sales Customer Relationship Management release notes
description: The ServiceNow Business Portal application enables your B2B customers to place orders, request quotes, and get support for orders and invoices through a self-service web portal. Business Portal was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Customer self-service for Sales Customer Relationship Management release notes

The ServiceNow® Business Portal application enables your B2B customers to place orders, request quotes, and get support for orders and invoices through a self-service web portal. Business Portal was enhanced and updated in the Australia release.

## Business Portal highlights for the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   Resume and submit invoice cases in draft state.
-   Review invoice case line details relevant to how your case was created.

[Australia Patch 1](../quality/australia-patch-1.md)

-   Enable business-to-business \(B2B\) customers to create invoice dispute cases through AI-powered chat and voice assistants that guide them through conversational dispute intake on the Business Portal.
-   Provide uninterrupted handoff to human agents to support complex use cases, with full conversation context transferred to the CSM/FSM Configurable Workspace.

Australia Early Availability

-   Enable business-to-business \(B2B\) customers to create invoice dispute cases for quantity, pricing, or date discrepancies through an intuitive playbook experience.
-   Enable customers to view invoices and invoice details directly from the Business Portal, providing transparency into billing information.
-   Provide customers with visibility into invoice case status, resolution steps, and associated invoice lines to track dispute progress.

See Customer self-service for Sales Customer Relationship Management for more information.

**Important:** Business Portal is included with Customer Service Portal, which is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   **Resume and submit invoice cases in draft state**

    Pick up an invoice case where you left off by resuming draft invoice cases from the Business Portal. Use the Process tab on the Standard Ticket page to continue editing invoice case and invoice case line disputes, then submit for further processing.

-   **Context-aware invoice case line list view**

    Review invoice case line details that are relevant to how your case was created. The Business Portal displays request source-aware columns in the invoice case line list view, showing specific details when a case is raised for a single invoice or when it spans multiple invoices.


[Australia Patch 1](../quality/australia-patch-1.md)

-   **AI-powered invoice case management for customers**

    Enable customers to report invoice disputes through an AI-powered virtual assistant on the Business Portal. Customers can describe quantity-related discrepancies through natural conversation. The assistant validates details, creates cases, and autonomously resolves eligible disputes by issuing credit notes or replacement orders or connecting customers with a human agent when needed. Interaction channels include chat and voice options.

-   **Invoice dispute intake with voice assistant**

    Enable customers to report quantity-related invoice disputes using voice commands through an AI-powered voice assistant on the Business Portal. Customers can describe discrepancies through natural speech and the assistant captures dispute details to create invoice cases or connects customers with a human agent.

-   **Human agent handoff with context transfer**

    Help customers to escalate complex disputes seamlessly to a live agent. The full conversation context, including invoice details, dispute reason, and prior AI actions are transferred to the CSM/FSM Configurable Workspace, enabling live agents to continue without asking customers to repeat information.

-   **Now Assist for invoice case resolution**

    Help accelerate invoice dispute resolution by surfacing similar cases and common resolution patterns in the Now Assist panel. Agents can request help with an invoice case to view how similar disputes were resolved, reducing research time and improving consistency.

-   **Automated email notifications for invoice cases**

    Keep customers informed with automated email notifications at key points in the invoice case life cycle, including case creation confirmation, resolution details with credit note or replacement order information, and the next steps for cases requiring human review.


Australia Early Availability

-   **Invoice management on Business Portal**

    Enable your customers to view invoices and invoice line details directly on the Business Portal, providing transparency into quantity, billing location, shipping location, and sold product information.

-   **Invoice case creation through playbook experience**

    Provide self-service capability to your customers to create invoice dispute cases directly from the Business Portal for quantity, pricing, or date discrepancies using a guided self-service experience, supporting both single invoice and multiple invoice scenarios.

-   **Invoice case management on Business Portal**

    Enable your customers to view and track invoice cases on the Business Portal, reducing support inquiries and keeping them informed on dispute resolution progress.


## Activation information

The Business Portal application \(sn\_b2b\_portal\) is automatically installed when you install the Customer Service Portal \(sn\_csm\_portal\). Install the Customer Service Portal by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   [Australia Patch 1](../quality/australia-patch-1.md)

        Manage Invoice Operations \(com.sn\_inv\_ops\_aias\): Delivers AI-powered assistants that handle invoice dispute intake directly from the portal, resolves eligible cases autonomously, and seamlessly escalates to a human agent when needed. In the workspace, it continues to assist human agents by providing relevant insights and actions to accelerate invoice case resolution.

    Australia Early Availability

    -   Invoice Self-Service \(com.sn\_invoice\_ss\): Enable an efficient invoice management experience for B2B customers on the Business Portal, helping them to view and manage invoices efficiently and improve financial operations.
    -   Invoice Case Self-Service \(com.sn\_invoice\_case\_ss\): Enable B2B customers to monitor and manage invoice-related cases efficiently through the Business Portal.
    -   Invoice Case Playbook \(com.sn\_inv\_case\_pb\): Enable a secure, guided playbook experience for B2B customers on the Business Portal to create and manage invoice-related cases.

## Related ServiceNow applications and features

-   **Case Management for Invoice Operations**

    The Case Management for Invoice Operations application enables customer service agents to create and manage cases for specific lines from a single invoice or for multiple invoices.

-   **Now Assist for Order Management**

    Use the ServiceNow® Now Assist for Order Management application to improve agent and customer productivity and efficiency in their respective workflows.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

