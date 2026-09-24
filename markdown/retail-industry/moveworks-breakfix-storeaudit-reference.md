---
title: Components Moveworks Integration for Break-Fix and Store Audit
description: Technical details on data flow, integration points, API usage, and supported operations for Moveworks with Break-Fix Case Management and Store Audit Plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/moveworks-breakfix-storeaudit-reference.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 3
breadcrumb: [ServiceNow Otto for Break-Fix and Store Audit overview, ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# Components Moveworks Integration for Break-Fix and Store Audit

Technical details on data flow, integration points, API usage, and supported operations for Moveworks with Break-Fix Case Management and Store Audit Plans.

## Data Integration Model

**System of Record:** ServiceNow RSM remains the authoritative source for all Break-Fix and Store Audit data. Moveworks reads/writes via NOW MCP server; no data replication occurs.

**Integration Layer:** NOW MCP server provides API bridge between Moveworks and ServiceNow RSM. All Moveworks operations \(case creation, status lookup, tracking\) route through NOW MCP.

|**Operation**|**Break-Fix**|**Store Audit**|
|-------------|-------------|---------------|
|Create Case|Moveworks → NOW MCP → RSM Break-Fix Case|Plan published via RSM UI \(auto-generates cases\)|
|Read Status|Moveworks ← NOW MCP ← RSM Break-Fix Case|Moveworks ← NOW MCP ← RSM Audit Case|
|Update Case|Add comment, extend date, reassign → NOW MCP → RSM|Task completion \(Pass/Fail\) → Mobile → RSM \(via FSM\)|
|Notifications|RSM status change → NOW MCP → Moveworks → Chat|Plan/Task status change → NOW MCP → Moveworks → Chat|

## Break-Fix Case Integration with Moveworks

**Case Creation:** Moveworks extracts store ID \(from user profile\), equipment type \(from NLP\), and severity \(from conversation context\). Sends to RSM via NOW MCP. Case created with category=Break-Fix, correct priority, and full conversation context attached.

**Metadata Mapping:**

-   **Store ID:** User profile → Buyer Organization \(Service Organization match\)
-   **Equipment Type:** NLP extraction → RSM equipment category
-   **Severity:** Conversation analysis → Priority \(Critical/High/Medium/Low\)
-   **Requester:** Moveworks identity → User lookup in RSM
-   **Context:** Full conversation transcript → Case description field

**Knowledge Base Integration:** Moveworks queries RSM KB via NOW MCP for troubleshooting steps matching equipment type and issue keywords. Steps ranked by relevance and presented in chat before case escalation.

**Case States and Transitions:** Cases follow standard Break-Fix state machine \(New → Acknowledged → In Progress → Resolution Proposed → Closed\). Moveworks displays current state and available actions \(add comment, extend due date, reassign\).

**HQ Support Integration:** Cases arrive in RSM with proper categorization and full context, reducing triage time compared to portal submissions with dropdown errors.

## Supported Operations by Workflow

**Break-Fix via Moveworks:**

-   Create case \(natural language submission\)
-   View troubleshooting steps \(KB search\)
-   View case status \(single or consolidated list\)
-   Add comments to case
-   Extend due date
-   Reassign fulfiller
-   Receive status change notifications
-   Doesn't create incident/work order \(stays in RSM workflow\)
-   Doesn't directly dispatch technician

## Channels and Availability

All Moveworks operations for Break-Fix and Store Audit available across:

-   **Web Portal:** Full chat, case creation, status tracking
-   **Microsoft Teams:** Full chat, case creation, status tracking via bot
-   **Slack:** Full chat, case creation, status tracking via bot
-   **Embedded Retail Portal:** Chatbot widget within Retail portal for Break-Fix and Store Audit queries

**Mobile Access:** Teams and Slack mobile apps provide Moveworks access on mobile. Store Audit task execution still occurs on dedicated mobile app.

## Data Scope and Limitations

**Store Data Isolation:** Users can only see/manage cases and audits for their assigned store. Moveworks enforces store-level access control via user profile \(Buyer Organization\).

**Role-Based Access:** Store staff can submit Break-Fix cases and view audit progress. HQ support views all cases in queue \(role-based access in RSM enforced via NOW MCP\).

**Conversation History:** Moveworks conversation transcripts retained in Moveworks; full case context also stored in RSM case description and comments.

**Historical Data:** Moveworks can retrieve and display past cases and audit results from RSM up to 12 months \(configurable\).

## Error Handling and Fallback

**NOW MCP Unavailable:** If NOW MCP server is down, Moveworks informs users that case operations are temporarily unavailable and suggests using RSM portal instead.

**Metadata Extraction Failure:** If Moveworks cannot extract equipment type or severity from conversation, it prompts user to clarify \(example: "What type of equipment is failing?"\) before case creation.

**Portal Fallback:** All Break-Fix and Store Audit operations remain available in RSM portal. Moveworks is alternative interface; users can switch to portal anytime.

**Parent Topic:**[ServiceNow Otto for Break-Fix and Store Audit overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-storeaudit-overview.md)

**Related topics**  


[Components for Break-Fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/breakfix-reference.md)

[Components installed with Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-store-audit-reference.md)

