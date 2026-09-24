---
title: Reviewing policy enforcement in AI Control Tower
description: Review policy activities and execution results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-pol-reviewing-enforcement-activity.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, Policies, enforcement activity]
breadcrumb: [Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Reviewing policy enforcement in AI Control Tower

Review policy activities and execution results.

## Key benefits

-   Confirm a policy actually reached every point it applied to.
-   Tell a real failure apart from a policy that simply didn't apply anywhere it could.
-   Look up a specific person or asset, without checking policies one at a time.

View policy enforcement as an audit trail in the **Enforcement activity** tab. Each entry represents enforcement against one asset and shows its outcome. When a policy triggered the entry, the entry also shows which policy. A policy that enforces through more than one connector produces a separate entry for each connector.

For AI agent containment specifically, the **Enforcement activity** tab shows all agents that were contained automatically through a Threat Response policy, and those contained manually using kill switch protocol. Those contained manually show Kill Switch Manual Trigger in the **Source** column.

An outcome other than success has a specific meaning, not just pass or fail:

-   **Error** means something actually went wrong at a connector, and the record includes why.
-   **Skipped** means no connector applied to that context, either because there was nothing to enforce against, or because the connector for that point was never configured. If you expected enforcement at a given point and see **Skipped**, confirm that point is configured and active on the **Control enforcement points** tab; otherwise, a real coverage gap can look like a clean run. See [Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-security-connections.md).
-   **Timeout** means a connector didn't respond within its window.

## Use cases

-   Confirm whether a particular person was blocked from a particular model, and which connector enforced it.
-   Check an entry to determine whether a policy needs to be fixed. An outcome other than success can mean the policy simply didn't apply rather than failed.
-   When a user reports they've lost access, or a security review needs to know whether a specific asset has been affected by any policy, filter the activity by that person or asset.

To create or change a policy, see [Managing policies in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-pol-managing-policies.md).

