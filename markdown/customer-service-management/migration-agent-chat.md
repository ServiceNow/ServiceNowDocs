---
title: Agent Chat for CSM Configurable Workspace
description: Learn how the CSM Agent Workspace Agent Chat functions with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-agent-chat.html
release: australia
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Agent Chat for CSM Configurable Workspace

Learn how the CSM Agent Workspace Agent Chat functions with CSM Configurable Workspace.

Agent Chat enables agents to interact with customers, create incident or case records, or transfer chats to another agent or queue. CSM Agent Workspace Agent Chat configurations work with CSM Configurable Workspace.

No rebuild is required, but if your CSM Agent Workspace deployment used custom chat workflow configurations, verify that they're still correct after migration.

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
</table>**Note:** You can't change parameters that are hidden in UI Builder through the UI Builder interface. If you need to change these values, contact ServiceNow Customer Support.

## Verify Agent Chat after migration

Role required: admin

1.  Open a chat interaction in CSM Configurable Workspace and confirm that the Agent Chat component displays correctly.
2.  Confirm that agents can receive and respond to chat messages, create case records from chat, and transfer chats to another agent or queue.
3.  If Agent Chat doesn't appear, navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**, open the CSM/FSM Configurable Workspace experience, and verify that the Agent Chat component is on the interaction record page.

