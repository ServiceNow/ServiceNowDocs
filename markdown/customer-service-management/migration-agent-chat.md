---
title: Agent Chat for Customer Service Management Configurable Workspace
description: Learn how the CSM Agent Workspace Agent Chat functions with CSM Configurable Workspace.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Agent Chat for Customer Service Management Configurable Workspace

Learn how the CSM Agent Workspace Agent Chat functions with CSM Configurable Workspace.

Agent Chat enables agents to interact with customers, create incident or case records, or transfer chats to another agent or queue. CSM Agent Workspace Agent Chat configurations work with CSM Configurable Workspace.

For more information about the Agent Chat component, see [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades) and select Agent Chat from the list of Next Experience Components.

## Agent Chat corresponding parameters

Parameters that are hidden in UI Builder \(UIB\) aren’t configurable in UIB. These parameters are used for specific customer workflow use cases.

<table id="table_usb_qrl_v4b"><thead><tr><th>

Component

</th><th>

Legacy component name

</th><th>

Legacy component parameter name

</th><th>

UIB component parameter name

</th></tr></thead><tbody><tr><td>

Agent Chat

</td><td>

sn-chat

</td><td>

Interaction - Active

</td><td>

-   Interaction Sys ID - Active \(Hidden in UIB\)
-   User isUxf \(Hidden in UIB\)

</td></tr></tbody>
</table>