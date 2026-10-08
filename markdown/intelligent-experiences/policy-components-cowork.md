---
title: Policy components in ServiceNow Cowork
description: A ServiceNow Cowork policy has seven components, each controlling a different part of what the agent can do.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/policy-components-cowork.html
release: zurich
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [policy components, tool gates, approval patterns, network rules, sandbox rules, file type rules, connector scopes, capabilities]
breadcrumb: [Policy management and governance in ServiceNow Cowork, Explore Cowork, ServiceNow Cowork, Enable AI experiences]
---

# Policy components in ServiceNow Cowork

A ServiceNow Cowork policy has seven components, each controlling a different part of what the agent can do.

Each component is a separate record that you link to a policy from its tab on the policy record.

## Default policy components

Every instance includes the **Default Policy**. It's active, applies to all users, and has values for all seven components.

|Component|Tab|Table|What it controls|
|---------|---|-----|----------------|
|Tool gates|**Policy Tool Gates**|sn\_app\_cowork\_tool\_gate|Sets each tool to **Allow**, **Deny**, **HITL**, or **Auto**.|
|Approval patterns|**Policy Patterns**|sn\_app\_cowork\_approval\_pattern|Defines which commands need a human decision, and whether the decision can be remembered \(soft gate\) or must be made every time \(hard gate\).|
|Network rules|**Policy Network Rules**|sn\_app\_cowork\_network\_rule|Lists the hosts and ports the sandbox can reach. Anything not on the allowlist is unreachable.|
|Sandbox rules|**Policy Sandbox Rules**|sn\_app\_cowork\_sandbox\_rule|Sets the sandbox filesystem boundary and network permissions for individual binaries. Rules can restrict access further but can't loosen the built in protection of credential paths and system directories.|
|File type rules|**Policy File Type Rules**|sn\_app\_cowork\_file\_type\_rule|Sets read, write, or deny access for each file extension.|
|Connector scopes|**Policy Connector Scopes**|sn\_app\_cowork\_connector\_scope|Turns OAuth scopes on or off for each connector. Microsoft 365 is supported. By default, read scopes are on and send and write scopes are off.|
|Capabilities|**Capability Overrides**|sn\_app\_cowork\_capability, sn\_app\_cowork\_capability\_override|Feature switches and numeric limits, such as subagents, auto approval, the feedback URL, and MCP override. Overrides change a capability's value for the users a policy covers.|

For how each tool gate setting handles an action, see [Action approval flow in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/action-approval-flow-cowork.md).

**Parent Topic:**[Policy management and governance in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/policy-management-cowork.md)

