---
title: Catalog auto submission
description: When the L1 IT Service Desk AI Specialist drafts or submits catalog requests with required variables, it uses the variable collection mechanism to collect the information needed to complete the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/catalog-variable-collection-slot-fill-l1-sd-ai-spec.html
release: brazil
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 3
keywords: [variable, slot filling, catalog, collection, mandatory]
breadcrumb: [Explore, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Catalog auto submission

When the L1 IT Service Desk AI Specialist drafts or submits catalog requests with required variables, it uses the variable collection mechanism to collect the information needed to complete the request.

## How variable collection works

Most service catalog items require information from the requester before they can be fulfilled. These are called variables. For example, a software license request might require the employee ID, department, and software product version. The L1 IT Service Desk AI Specialist uses variable collection to gather this information efficiently.

When the L1 IT Service Desk AI Specialist identifies that an incident matches a catalog item, it:

1.  Determines which variables are required for that catalog item
2.  Auto-fills variables it can determine from available context \(incident details, requester profile, interaction history\)
3.  Asks the requester to provide values for remaining required variables
4.  Continues the conversation to collect any additional variables that is set to required after initial values are supplied

## Auto-fill process

The L1 IT Service Desk AI Specialist attempts to populate variables automatically before asking the requester for input. This reduces the number of interactions needed and speeds up request submission.

The AI specialist only fills a variable if the value can be confirmed from available context. An unfilled variable is preferable to an incorrect one, as an incorrect value can delay fulfillment or cause the request to be rejected.

## Conditional variable exposure

Some catalog items have conditional variables. The set of required variables changes based on answers to earlier questions.

**Note:** For example, a hardware request might ask "What type of device?" first, and then ask different follow-up questions depending on whether the requester selected laptop, desktop, or mobile device.

The L1 IT Service Desk AI Specialist handles this multi-turn conversation automatically. After the requester answers each question, the AI specialist determines which new variables are now required and asks for them in the next turn.

The L1 IT Service Desk AI Specialist asks each question by posting it as a comment on the incident and waiting there for the requester's reply. The requester has up to 24 hours to answer each question before that turn times out.

## Collection interaction limits

To prevent prolonged back-and-forth conversations, the L1 IT Service Desk AI Specialist has limits on how many clarification exchanges it will attempt before escalating to a human service desk agent. If the requester does not respond or consistently provides incomplete information, the AI specialist:

-   Records what information was successfully collected
-   Documents what required variables remain unfilled
-   Routes the incident to the service desk team with a work note describing the collection state

This helps prevent incomplete or stalled requests from remaining unresolved.

## Product catalog items with variables

Beyond standard service catalog items, the L1 IT Service Desk AI Specialist also handles Product Catalog Items \(hardware and software\) that carry variables. These orderable items are configured similarly to standard catalog items, with their own sets of required and optional variables. Variable collection applies the same logic to product catalog requests as to service catalog requests.

## Auto-fill and auto-submit for incident-linked catalog requests

When the L1 IT Service Desk AI Specialist matches an incident to a catalog item, the catalog item's variables are pre-filled on the request form automatically. For example, an incident requesting a virtual machine with 8 GB RAM, 2 CPUs, and 40 GB storage is matched to the VM Provisioning catalog item, and those three values are pre-filled on the drafted request.

What happens next depends on the **Auto-submit catalog requests** setting and whether all required variables were filled:

-   If auto-submit is active and all mandatory variables are filled \(or there are none\), the L1 IT Service Desk AI Specialist submits the request automatically. The incident is placed on hold, awaiting the request outcome.
-   If auto-submit is active but a mandatory variable can't be determined, the L1 IT Service Desk AI Specialist asks the requester for it directly on the incident instead of drafting the request. See [Conditional variable exposure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/catalog-variable-collection-slot-fill-l1-sd-ai-spec.md).
-   If auto-submit is inactive, the L1 IT Service Desk AI Specialist drafts the request regardless of whether the variables are filled. It sends the requester a link to review, complete, and submit it.

After the requester submits the drafted request, the linked incident is automatically resolved with a resolution code that references the request number.

\[Omitted image "l1-catalog\_slot-fill-resolution.png"\] Alt text: Incident activity showing AI-generated resolution notes and a customer comment describing the drafted VM Provisioning request.

