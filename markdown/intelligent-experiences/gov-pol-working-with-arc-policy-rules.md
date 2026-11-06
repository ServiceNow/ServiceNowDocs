---
title: Working with Arc policy rules
description: Add and customize the rules that control what Arc can do for the users a policy covers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-working-with-arc-policy-rules.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, arc policy rules, tool gates, approval patterns, capability overrides]
breadcrumb: [Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Working with Arc policy rules

Add and customize the rules that control what Arc can do for the users a policy covers.

Each rule you add to a policy changes one part of the default behavior of Arc, such as which tools it can use or which actions need approval.

-   Tool gates and approval patterns work together to decide which actions wait for a person's approval. Before you create tool gates and approval patterns, see [Action approval flow in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-action-approval-flow.md).
-   Network, file type, sandbox, and connector scope rules limit what an action can reach once it runs.
-   Capability overrides change which features Arc offers users.

## Choosing a rule type

|Goal|Rule type|
|----|---------|
|Block a tool, or send its calls for review|[Tool gate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-tool-gate.md)|
|Require approval for specific commands, or let trusted commands run without a prompt|[Approval pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-approval-pattern.md)|
|Open or close a network destination|[Network rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-network-rule.md)|
|Keep the agent from reading or changing certain types of files|[File type rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-file-type-rule.md)|
|Limit which paths the sandbox can read or write, or which programs in it can reach the network|[Sandbox rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-sandbox-rule.md)|
|Limit what the agent can do through a connector, such as sending email|[Connector scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-connector-scope.md)|
|Turn a feature on or off, or change a limit, such as auto mode or how long a task can run|[Capability override](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-capability-override.md)|

