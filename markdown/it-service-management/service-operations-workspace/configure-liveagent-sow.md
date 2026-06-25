---
title: Live Agent chat in Service Operations Workspace
description: Service Operations Workspace enables agents to work on any incident created using Live Agent chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/configure-liveagent-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Live Agent chat in Service Operations Workspace

Service Operations Workspace enables agents to work on any incident created using Live Agent chat.

An application admin can integrate the Live Agent into the ServiceNow application by installing the com.glide.interaction.awa plugin. For more information about installing and enabling a plugin, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

After the plugin installation, an inbox icon \[Omitted image "inbox-icon.jpg"\] Alt text: Inbox icon. appears in the sidebar of the Service Operations Workspace window.

By default, the status of the agent is Offline. To start the communication, the agent must modify the status to Available.

When the customer reports an incident through Live Agent \(for example, through the Service Portal\), an incident is created automatically in the Inbox. The agent can then work on the incident by selecting **Accept** and chat with the user simultaneously to resolve the issue.

\[Omitted image "incoming-chat-ims.png"\] Alt text: Live agent chat

Once the agent accepts the chat, the Inbox is hidden, allowing the agent to focus on resolving the incident.

\[Omitted image "chat-hidden-ims.png"\] Alt text:

For more information about Live Agent chat integration, see [Move from Connect Support to Advanced Work Assignment and Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/migrate-from-connect-support.md).

**Parent Topic:**[Operating IT services in your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/enhancing-services-operations-in-organization.md)

**Related topics**  


[Play a guided tour in Service Operations Workspace]()

[Add a user-specific quick link on the ITSM landing page]()

[Create a list in Service Operations Workspace]()

[Interaction Management in Service Operations Workspace]()

[Incident Management in Service Operations Workspace]()

[Request Management in Service Operations Workspace]()

[Change Management in Service Operations Workspace]()

