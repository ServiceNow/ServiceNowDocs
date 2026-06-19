---
title: Publish ServiceNow agents to Microsoft Agent 365
description: Make ServiceNow agents available in Microsoft Agent 365 so end users can discover and interact with them from the Microsoft ecosystem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/publish-servicenow-agents-to-microsoft-agent-365.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [AI asset inventory, AI assets, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Publish ServiceNow agents to Microsoft Agent 365

Make ServiceNow agents available in Microsoft Agent 365 so end users can discover and interact with them from the Microsoft ecosystem.

## Before you begin

Role required: AI steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **AI assets** &gt; **AI asset inventory**.

2.  Open an asset from the list.

    **Note:** Verify that the asset’s

    -   Lifecycle Phase is deployed
    -   Lifecycle State is deployed
    -   Lifecycle Status is deployed
    -   Asset type is agentic AI
    -   Management status is Managed
    -   System property is enabled
3.  Select **Publish to Microsoft Agent 365**.

4.  From the Credential drop-down, select the credential that authorizes calls to Microsoft Agent Resources.

5.  Select Publish.

    **Note:** A banner displays ‘Successfully initiated the publish to Microsoft Agent 365’ and the Deployment state changes to Deployed.


## Result

The ServiceNow agent is published to Microsoft Agent 365 and appears in the Microsoft agents portal for end users.

**Note:** To unpublish the agent, select Remove From Microsoft Agent 365.

