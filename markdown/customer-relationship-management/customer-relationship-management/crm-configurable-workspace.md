---
title: Configurable workspace
description: Configurable workspace is a user interface that provides users with the tools and information they need to assist customers. Workspaces use role-based layouts, components, and communication channels to support agent, fulfiller, and technician workflows across Sales CRM, CSM, FSM, and industry solutions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 4
---

# Configurable workspace

Configurable workspace is a user interface that provides users with the tools and information they need to assist customers. Workspaces use role-based layouts, components, and communication channels to support agent, fulfiller, and technician workflows across Sales CRM, CSM, FSM, and industry solutions.

## Configurable workspace overview

Configurable workspace is a flexible interface that displays tools and information for the tasks that a user needs to accomplish. The pages that appear in a workspace, such as landing pages, dashboards, and record pages, and the components that appear on a page, including record details, contextual side panel, and playbooks, are configured in UI Builder to support the user roles and the workflows of each organization.

![CSM Configurable Workspace interface provides information such as record details, the activity stream, and tools in the contextual side panel such as recommended actions and templates.](../image/csm-config-workspace-interface.png "CSM Configurable Workspace")

Configurable workspace is built on a shared component registry, which means that capabilities configured for one product context can be made available in others across the CRM suite. Configurable workspace serves as the primary interface for agents, fulfillers, and technicians in Sales CRM, CSM, FSM, and industry solutions built on the ServiceNow platform.

## Configurable workspace benefits

Configurable workspace provides benefits to internal users across an organization.

-   **For agents, fulfillers, and technicians:** Record pages in a configurable workspace can reduce the time agents, fulfillers, and technicians spend to understand record context and locate information. Customer details, case or work order history, SLA status, communication tools, and resolution guidance are available in a single interface without having to switch screens. The workspace configuration directly shapes what these users see and how efficiently they can respond.
-   **For administrators and implementation partners**: Configurable workspace provides configuration options based on unique workflows and user tasks. Case types, roles, and product lines can have independent record pages with their own layouts and components, all managed within UI Builder. New record pages can be created from templates or existing pages and configured independently without modifying existing configurations.

## Products and contexts

Each product within the CRM portfolio uses configurable workspace as the foundation for its primary work interface.

-   **Sales CRM**

    Sales CRM users use configurable workspace to manage leads, opportunities, quotes, and orders across the sales cycle. Administrators can configure workspace record pages by roles such as sales rep, sales ops, fulfiller, or support agent to surface the objects and actions most relevant to each persona. Components such as Customer 360, which surfaces account details, open quotes, order history, contracts, install-base items, and entitlements, gives users full visibility into the customer relationship at every stage, from pre-sale through fulfillment.

-   **CSM**

    Customer service agents use configurable workspace to manage cases, customer interactions, and service operations. Administrators can configure workspace record pages by case type, role, and communication channel to reflect the organization's service model. Components such as Customer 360, which surfaces customer account details, case history, and installed products, can be added to record pages where the underlying customer data supports it.

-   **FSM**

    Configurable workspace serves both dispatchers managing work order queues and field service technicians working from mobile devices. Both experiences are configured in UI Builder using the same framework as CSM, which means administrators managing both CSM and FSM configurations work within a consistent toolset.

-   **Industry solutions**

    Telecommunications, financial services, and manufacturing solutions include preconfigured workspace page layouts, components, and playbooks tailored to the workflows common in those industries. Organizations can deploy these preconfigured experiences as a starting point and modify them in UI Builder as requirements evolve.


## Use cases

-   **Customer service: communication channel interactions**

    A customer service organization creates separate workspace record pages for agents handling interactions from different communication channels, including chat, voice, and email. Each record page uses a layout designed for efficient customer communication. For example, chat interactions put the chat component in the center of the workspace and display the chat history alongside. Voice interactions include a voice component that can be integrated with Contact Center as a Service \(CCaaS\) providers.

    When customer service agents field interactions with customers, the workspace automatically displays the right record page for the channel type so agents can engage with customers, gather information, and reach resolutions faster.

-   **Field service: telecommunications**

    A telecom provider uses configurable workspace to support both a central dispatch team and field technicians. Dispatchers see a landing page oriented around work order queues and SLA exposure. Technicians see a mobile-optimized workspace with work order details, customer history, and parts availability.

    Both experiences are configured and maintained within the same UI Builder application, which enables a single administrator to manage workspace configurations for both teams without context-switching between different tools or frameworks.

-   **Financial services: consumer banking**

    A retail bank configures separate workspace layouts for agents handling current accounts, mortgages, and credit card cases. Each case type has its own record page, components, and contextual side panel configuration. The mortgage complaint case type includes a playbook that guides agents through the bank's complaint handling process, components that surface escalation status and active SLA, and a Customer 360 panel showing the customer's account and interaction history.

    When the bank adds a fraud disputes team, the implementation partner configures a new record page for the case type, with its own playbook, routing rules, and landing page, without modifying existing configurations for other product lines. Advanced Work Assignment routes incoming fraud cases to agents with the appropriate skill designation.

-   **Manufacturing: after-sales service**

    A manufacturer uses an industry solution workspace preconfigured for after-sales service operations. The implementation team deploys the preconfigured layouts for the case management and field dispatch teams, then modifies the ribbon component configuration for the field team to surface installed product records and warranty status relevant to their work. The preconfigured playbooks are retained for standard warranty cases and extended for the manufacturer's escalation workflows using UI Builder.


## Related topics

**Related topics**  


[CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspaces-configure.md)

[CSM Configurable Workspace features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspace-feature-overview.md)

[CSM Configurable Workspace record pages and page templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-ws-pages-templates.md)

