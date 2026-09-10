---
title: L1 APO Service Desk Specialist
description: The L1 APO Service Desk Specialist is a worker agent that processes incoming invoice inquiries using knowledge articles and historical data. The AP agents to focus on more complex work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/l1-apo-service-desk-specialist.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-14"
reading_time_minutes: 2
keywords: [L1 APO Service Desk Specialist, autonomous worker, invoice inquiries, agentic AI, pre-built skills]
breadcrumb: [AI L1 APO Service Desk Specialist, Use AI agents in ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# L1 APO Service Desk Specialist

The L1 APO Service Desk Specialist is a worker agent that processes incoming invoice inquiries using knowledge articles and historical data. The AP agents to focus on more complex work.

The Zero Touch Service Desk \(ZTSD\) for APO enables AI L1 Service Desk automation for inquiry cases through a flexible, agentic AI architecture.

## Capabilities

The L1 APO Service Desk Specialist uses pre-built skills and AI agents to:

-   Classify and triage incoming invoice inquiry cases
-   Investigate invoice details and related records
-   Generate and deliver resolutions autonomously
-   Communicate updates to suppliers and employees
-   Escalate cases to human agents when AI confidence is low

## How it works

A requester submits inquiry case through channels such as web, email, virtual agent, mobile, and manual entry. Invoice case is automatically assigned to AI L1 APO Service Desk Specialist through assignment rules. The worker agent searches knowledge base articles, historical data and the confidence score \(&gt;70 threshold\) to generate resolutions and close the case automatically or escalate to AP specialist for further analysis. When ZTSD is inactive or paused, the worker agent can resume processing the AP case anytime and provide case resolution without human intervention.

The following steps describe how the L1 APO Service Desk AI Specialist processes invoice inquiry.

1.  A user submits invoice inquiry through supplier portal.
2.  The system checks whether the L1 APO Service Desk AI Specialist is active.

    **Note:** If the agent is not active, the request proceeds with the standard triage process and the following steps do not apply.

3.  The request is assigned to the L1 APO Service Desk AI Specialist.
4.  The L1 APO Service Desk AI Specialist agent triggers and searches knowledge base articles and previously resolved invoice case requests for a resolution.
5.  The agent processes the request based on the search results:
    1.  Resolution found: The agent posts the resolution to the activity stream and changes the request state to Closed Complete.
    2.  Resolution could not be found: The agent posts notes to the activity stream, changes the request state to New, clears the Assigned to field, and assigns case to AP specialist.

## Key components

The following table describes the key components of the L1 APO Service Desk Specialist.

## Plugins

To access the AI L1 APO Service Desk Specialist, the following plugins must be installed:

-   ServiceNow Otto for Accounts Payable Operations \(APO\)
-   Zero Touch Service Desk plugin \(`com.snc.sn_ztsd`\)

## Knowledge sources

The L1 APO uses AI search profile to search the knowledge base articles, previously published articles, historical data for effective case resolution.

