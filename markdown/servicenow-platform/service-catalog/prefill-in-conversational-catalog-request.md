---
title: Prefill in conversational catalog request
description: The generalized prefill capability for conversational catalog request automatically populates catalog item form fields using data sourced from the requesting user's profile and from the active chat conversation history. This reduces manual data entry for requesters, improves form completion accuracy, and accelerates time-to-submission for service requests raised through the conversational interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-catalog/prefill-in-conversational-catalog-request.html
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-04-24"
reading_time_minutes: 1
breadcrumb: [LLM topic blocks, Conversational Catalog Requests reference, Conversational Catalog Requests, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Prefill in conversational catalog request

The generalized prefill capability for conversational catalog request automatically populates catalog item form fields using data sourced from the requesting user's profile and from the active chat conversation history. This reduces manual data entry for requesters, improves form completion accuracy, and accelerates time-to-submission for service requests raised through the conversational interface.

Prefill functionality works similarly across both conversational and traditional form-based catalog experiences, automatically populating fields to reduce manual data entry and improve accuracy. The same underlying prefill sources and behavior apply whether requesters use ServiceNow Otto conversations or standard web forms.

## User profile prefill

System fields on the catalog item form are automatically populated from the requester's sys\_user and related tables. This includes, but is not limited to:

-   Identity fields: First name, last name, display name, email address
-   Organizational fields: Department, cost center, company, location, building, floor
-   Managerial fields: Manager, secondary approver Role or group-based fields: Primary assignment group, business unit

## Conversation context prefill

In conversational catalog requests, the system extracts contextual information surfaced during the ongoing chat conversation and uses it to pre-populate relevant catalog item variables. For example, if a requester:

-   Mentioned an affected asset \("my laptop with serial number X"\), that value prefills the appropriate configuration item field.
-   Stated an urgency or preferred resolution date, those values prefill date or priority fields on the catalog item.
-   Described a business justification or request reason earlier in the conversation, that text prefills a description or justification variable.

**Parent Topic:**[LLM topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-catalog/llm-topic-blocks-reference.md)

**Related topics**  


[Prefilling variable values on the catalog item form in the portal and Next Experience UIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-catalog/prefill-variable-values-catalog-item-form.md)

