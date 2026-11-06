---
title: Catalog auto submission
description: When the L1 IT Service Desk AI Specialist drafts or submits catalog requests with required variables, it uses the variable collection mechanism to collect the information needed to complete the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/catalog-variable-collection-slot-fill-l1-sd-ai-spec.html
release: australia
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 6
keywords: [variable, slot filling, catalog, collection, required]
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

## Catalog submission employee engagement

When the L1 IT Service Desk AI Specialist matches an incident to a catalog item and needs more information to submit, it asks the requester for the missing details. By default, it writes these messages dynamically, based on the details it already has and the details it still needs, so each message fits the request instead of repeating fixed text.

By default, the L1 IT Service Desk AI Specialist:

-   Greets the requester by first name, thanks them for contacting IT Support, and names the catalog item in the first message. Later messages acknowledge the requester's reply instead of greeting again.
-   Lists the details it already has, using short labels and plain-language values. It marks any value the requester just changed, leaves out **Requested for** when it's the requester, and leaves out values it can't show as readable text.
-   Asks for the remaining required details in plain language, numbered when there's more than one. It includes valid options in the question, and explains what to fix if an earlier answer wasn't accepted.
-   Closes by saying what happens next. It never says the request is submitted while details are still needed.
-   Supports basic formatting such as paragraphs, line breaks, bold, and italic. Other markup, including markup typed by the requester, appears as plain text.

## If a message can't be composed

In Dynamic mode, if the L1 IT Service Desk AI Specialist can't compose a message, it posts the template's body instead. The template always appears in this case.

## Changing the mode or instructions

The messages come from two templates in the `sn_ztsd_agent_template` table:

-   `Engagement Request - Q&A`: the first message asking for missing details.
-   `Engagement Request - Q&A Follow-up`: later messages, after the requester replies.

Both templates use Dynamic mode by default. In Dynamic mode, the template's generation instructions control the message, including any format or wording they specify. In Template mode, the L1 IT Service Desk AI Specialist posts the text in the template's body field and fills in only the placeholders.

These templates don't appear in the **Response templates** setting on the task settings page. To change them, open the template record in the `sn_ztsd_agent_template` table:

-   To switch between Dynamic and Template, change the **Generation mode** field.
-   To change how messages read in Dynamic mode, edit the **Generation instructions** field.

You need the AI Worker Manager \[sn\_aia.worker\_manager\] role.

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

-   If auto-submit is active and all required variables are filled \(or there are none\), the L1 IT Service Desk AI Specialist submits the request automatically. The incident is placed on hold, awaiting the request outcome.
-   If auto-submit is active but a required variable can't be determined, the L1 IT Service Desk AI Specialist asks the requester for it directly on the incident instead of drafting the request. See [Conditional variable exposure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/catalog-variable-collection-slot-fill-l1-sd-ai-spec.md).
-   If auto-submit is inactive, the L1 IT Service Desk AI Specialist drafts the request regardless of whether the variables are filled. It sends the requester a link to review, complete, and submit it.

The link opens in the portal that you select in the **Requester reference portal** setting. For more information, see [Response formatting fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md).

With an AIUX portal, the L1 IT Service Desk AI Specialist doesn't create a draft or ask the requester follow-up questions on the incident. It fills the variables once. If auto-submit is active and it filled every required variable, it submits the request. Otherwise, it sends a link to the catalog item, and a request exists only if the requester submits it.

After the requester submits the drafted request, the linked incident is automatically resolved with a resolution code that references the request number.

\[Omitted image "l1-catalog\_slot-fill-resolution.png"\] Alt text: Incident activity showing AI-generated resolution notes and a customer comment describing the drafted VM Provisioning request.

