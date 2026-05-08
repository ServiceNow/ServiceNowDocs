---
title: Domain separation and Virtual Agent
description: Domain separation is supported in the Virtual Agent application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [Virtual Agent, domain, separation, support]
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Domain separation and Virtual Agent

Domain separation is supported in the Virtual Agent application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see Application support for domain separation.

Domain separation allows you to partition your organization's data and administrative control into separate domains. This lets you isolate the data and control access to it, which is particularly important in environments where multiple tenants share a common platform.

Domain separation in Virtual Agent works by creating separate Virtual Agent views that are isolated from each other. The chat configuration, branding, NLU settings, and topics and components can be assigned to a given domain within Virtual Agent. Users within a domain can only access the Virtual Agent conversations that are associated with their domain. This means that users in one domain cannot access data or functionality that belongs to another domain, including Virtual Agent conversations. Additionally, administrators who are assigned to a domain cannot see or manage Virtual Agent conversations in other domains, ensuring complete separation and security.

Domain separation is best for customers with any of the following requirements:

-   You need to enforce absolute data segregation between business entities \(data separation\).
-   Customize business process definitions and user interfaces for each domain \(delegated administration\).
-   Maintain some global processes and global reporting in a single instance.
-   Separate data between customers or sub-organizations.
-   The session scope is set upon session establishment to the domain listed in the user's user record. Users can manually change their session domain scope with the domain picker.
-   The record scope uses the domain of the record and is active when viewing the form of any record.

    By default, the record scope takes precedence over the session scope so that users in higher-level domains adhere to each record's data and process constraints. However, these users can choose to expand or collapse the domain scope to show or hide data from other domains. For example, a user in the service provider \(SP\) global domain also has visibility into child domains such as the ACME domain. When looking at an incident record from the ACME domain, the user can choose to expand the domain scope to show values from the MSP domain or collapse the domain scope to show only record values that match the record's ACME domain.

    **Note:** Users always have access to data from domains that have been explicitly granted to them by domain visibility.


When domain separation is used, guest users are restricted to the domain used in the session. For custom chat channels, the domain of the [provider application](../task/create-channel-id-va-cccif.md) is used. For the chat widget, you can associate a domain ID with the chat portal. For details, see [Associate a domain ID with a chat portal](../task/associate-domain-id-chat-portal.md).

For more information, see Domain scope.

## Requirements

All domain support features require the Domain Support - Domain Extensions Installer \[com.glide.domain.msp\_extensions.installer\] plugin. For details, see Request domain separation.

## Configuring Virtual Agent with domain separation

-   **Branding**

    Service providers can create a [chat branding configuration](../../conversational-interfaces/task/ac-configure-chat-branding.md) per domain.

-   **[Chat experiences](va-conversation-settings.md)**

    Chat experiences, including the default experience and any custom experiences, allow for domain separation. Each chat experience profile belongs to a domain. Each child customization, such as a setup topic change, belongs to a domain. Each child customization implements system overrides so that sub-domains can override parent-domain customizations.

-   **NLU settings**

    Only one NLU service provider can be set per domain-separated instance for all Virtual Agent clients. The managed service provider \(MSP\) logs in as a global user for the domain to configure NLU. For details, see [Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md).


## Creating topics in subdomains in Assistant Designer

**Roles required:** admin or virtual\_agent\_admin

The service provider either logs in to one of the subdomains and creates and publishes topics or allows subdomain admin users to [create](../task/create-virtual-agent-topic.md) and [publish](../task/publish-virtual-agent-topic.md) their own topics.

Topic names within a domain must be unique, but Virtual Agent does allow you to create topics with the same name in other domains. For example, each domain might have a topic called **Greeting**.

Only service provider admins can do the following:

-   Activate Virtual Agent conversation plugins or store apps for other ServiceNow business applications, such as ITSM, CSM, or HRSD, to enable pre-built topics for the subdomain.
-   Assign roles on a particular subdomain to control which topics can be run by users.

Admin users assigned to the subdomain can do the following:

-   Create topics in the instance.
-   Be logged into the global domain and impersonate a user in the subdomain.
-   Publish all available topics in the subdomain to chat widgets and messaging applications.

## Domain separation in the chat widget channel

The chat widget does not support domain separation. However, you can provide a domain-separated chat experience in the chat widget channel by using separate, domain-separated portals. For example, you can create two separate support portals that are restricted to separate domains. Use the **domain\_id** in the portal script to designate the domain. This gets passed as the **sysparm\_domain\_id** parameter in the portal URL.

To configure the portal, see [Associate a domain ID with a chat portal](../task/associate-domain-id-chat-portal.md).

For information about URL parameters, see [Virtual Agent URL parameters](../reference/va-sysparm.md).

## Domain separation and Virtual Agent messaging app integrations

**Roles required:** admin or virtual\_agent\_admin

The domain-separated instance has one setup record for Slack, Microsoft Teams, Workplace, or Facebook Messenger.

Customers on the subdomain license either Slack, Microsoft Teams, or Workplace independently of the ServiceNow instance.

The admin of the subdomain installs the integrations within the subdomain and configures the appropriate credentials to access Virtual Agent from the third-party client. For details, see [Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md).

For Facebook Messenger, the admin manually configures the integration. For details, see [Conversational Integration with Facebook Messenger](messg-fbm.md).

-   **[Associate a domain ID with a chat portal](../task/associate-domain-id-chat-portal.md)**  
The Service Portal platform is not domain-separated, but you can create different versions of a portal and restrict each version's use to a single domain for chat purposes. For example, you could create two employee service portals and define a different domain for each.

**Parent Topic:**[Virtual Agent technical reference](va-advanced-technical-reference.md)

**Related topics**  


[Virtual Agent interaction records](va-interactions.md)

[Virtual Agent scripts](virtual-agent-scripts.md)

[Input data types in Virtual Agent topics](../reference/va-data-types.md)

[NLU system entities](../reference/nlu-system-entities.md)

[Virtual Agent URL parameters](../reference/va-sysparm.md)

[Latency feedback in Virtual Agent](../reference/latency-feedback.md)

[bundle-psec.domain-sep-landing-page]

