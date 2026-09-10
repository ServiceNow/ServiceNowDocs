---
title: Domain separation and AI Control Tower
description: Domain separation is supported for AI Control Tower. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-domain-separation.html
release: australia
topic_type: concept
last_updated: "2026-08-20"
reading_time_minutes: 8
keywords: [Now Assist, AI Agents, generative AI, agentic AI, domain separation, AI Control Tower, multi-tenant, MSP]
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# Domain separation and AI Control Tower

Domain separation is supported for AI Control Tower. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic\*

The support level is Basic but has some exceptions or special conditions.

-   Business logic: Ensure that data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   The user interface, cache keys, reporting, rollups, and aggregations all use the domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

Sample use case: When an SP uses chat to respond to a tenant-customer’s message, the client must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview

AI Control Tower helps you discover, govern, monitor, and measure the value of AI systems across your enterprise. If you manage multiple business units or client tenants from a shared instance, such as a managed service provider, domain separation lets you keep each tenant's AI assets, risk posture, security data, and value calculations distinct while administering the deployment from a single instance.

## How domain separation works in AI Control Tower

AI Control Tower provides Basic support for domain separation beginning with the September release, across all pillars: inventory and discovery, monitoring, risk, security, and value.

Some elements remain common across domains regardless of this support level: playbook rule and template definitions, flows, and the AI Control Tower interface itself are shared. The data and behavior described in the pillar sections later in this topic are specific to each domain.

Within a domain hierarchy, a parent domain's view generally combines its own domain with all of its child domains, while a child domain's view shows only that domain's own data. Configuration settings, such as evaluation metric sample rates and cost framework rates, are inherited from a parent or global domain by default, and you can override a setting for a specific domain without affecting the global default or other domains.

## How to set up domain separation for AI Control Tower

The base system provides built-in functionality to separate an instance by domain. After an instance is domain-separated, any application that supports domain separation can be installed on that instance.

The application inherits and operates within the domain-separated setup, provided that the application itself supports domain separation.

For example, an organization can host Customer A and Customer B on the same instance, while logically separating their data and access by domain. Customer A can see only its own data, and Customer B can see only its own data.

For more information, see [Domain separation setup and administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparationSetup.md).

## Use cases

The following sections describe how domain separation applies within each pillar of AI Control Tower.

## Inventory and discovery

For inventory and discovery, domain separation keeps each domain's AI assets distinct while giving administrators at a parent domain oversight across their child domains.

-   AI asset visibility follows the domain hierarchy. A user at a parent domain can see AI assets across all of its child domains, while a user at a child domain sees only the assets in that domain.
-   Automated discovery and connectors create records in the domain of the user who configures the connector, so discovered AI systems and connections from both ServiceNow and external platforms are associated with the correct domain.
-   External AI systems registered with an API key are added to the domain of the user who created the key. A warning helps prevent registering an asset in the wrong domain with a key issued to another domain.
-   Automation rules and their templates show both the current domain's own records and any records inherited from a parent domain that haven't been overridden, but only the rules created within the current domain actually run.
-   Asset tags are scoped by domain, so a tag created for an asset in one domain doesn't appear in another domain's asset views.
-   Shadow AI's detected services, usage events, and per-user and per-device usage aggregates are scoped by domain, so a detection made in one domain doesn't surface in another domain's view.
-   The AI services registry that Shadow AI checks to recognize a domain as an AI service is shared, not domain-separated, since whether something is an AI service doesn't depend on which tenant detected it.

## Monitoring

For monitoring, domain separation ensures that evaluation data, trace history, and configuration changes for one domain never surface in another domain's view, even when the underlying AI agent is scoped globally.

-   Aggregate evaluation metrics reflect only the domains a user can see: their own domain, any child domains, and the global domain. Metrics from sibling or parent domains are never included, even for a globally scoped AI agent.
-   Traces and sessions are scoped to the domain of the user who generated them, not the domain of the AI agent. Running a globally scoped agent from within a specific domain still creates a trace that only that domain can see.
-   Evaluation metric configuration, such as sample rates and trace API limits, is inherited from the global domain by default. Overriding a setting for a specific domain applies only to that domain and its children, without changing the global default or affecting other domains.

## Risk and compliance

For risk, domain separation isolates each domain's risk posture while letting administrators at a parent domain see and manage risk across their child domains.

-   Risk assessment tasks and controls, such as impact assessments, attestations, and policy exceptions, are scoped to the domain of the related AI asset. A user sees the tasks assigned within their own domain plus any tasks in the global domain, but not tasks in sibling domains.
-   Aggregate risk rating and classification for an asset reflect only the data in the currently selected domain, so a rating calculated for one domain's assets never includes another domain's data.
-   Risk dashboards, including the regulatory risk classification, governance posture summary, and risk heat map, filter by the selected domain and roll up through the domain hierarchy. A parent domain's view combines its own data with all of its child domains, while a child domain's view shows only its own data.
-   Asset intake and onboarding workflows keep related records, such as configuration items, business applications, and datasets, in the domain of the new asset. Approval routing and any tasks the onboarding playbook creates stay within that domain, so users in other domains don't receive related notifications.
-   AI model provider and data privacy settings, such as which model providers are allowed and how data overflow is handled, are configured per domain. A change made in one domain's settings doesn't affect another domain's configuration, and using a model outside a domain's allowed list is blocked.

## Security

Domain separation ensures that each domain's security posture reflects only its own AI assets and activity, while dashboards and metric detail pages still honor the domain hierarchy.

-   The AI asset security score is calculated from the AI assets in the currently selected domain, so each domain's score reflects only its own assets.
-   In the Activity Center, security tasks are scoped to the current domain, so a domain shows only the security tasks associated with assets in that domain.
-   The agent map and access issue details inherit the domain of the underlying asset or agent. Viewing a parent domain includes the agents and access issues from its child domains.
-   In Post-runtime metrics, threat detection data for both internal and external agents is scoped by domain, so the threat map and related guardrail data reflect only the current domain's activity.
-   Your top recommendations don't appear on the security dashboard in domain-separated instances, because its underlying data isn't domain aware. Instead, a Security events detected section is shown.
-   In Runtime metrics, Sensitive data input and Sensitive data anonymized metrics aren't shown for domain-separated instances.
-   Details for Privileged AI agents, Dormant AI agents, Access issues, Security events detected, Agent map, Post-runtime, and AI asset security score include a Domain column showing the domain the AI asset belongs to.

## Value

For value, domain separation lets each domain calculate productivity gains and cost savings using its own assumptions, while still rolling results up for domains that oversee multiple child domains.

-   Value templates, the formulas used to calculate productivity gains for a managed AI system, can be inherited from a parent domain or overridden for a specific domain. Overriding a template in a child domain doesn't change the calculation for the parent template or other domains.
-   Productivity gains and savings data roll up through the domain hierarchy. A parent domain's dashboard combines its own data with all of its child domains, while a child domain's dashboard shows only its own data.
-   Cost framework rates cascade from the global domain to child domains by default. Administrators can override rates for a specific domain without changing the global rate or other domains' rates.
-   Rate changes apply prospectively only. Savings and cost data already calculated under a previous rate aren't recalculated when the rate changes.

## Strategy and planning

For strategy and planning, domain separation keeps AI investment demands, epics, and goals within the domain where they originate.

-   AI investment demands, and the epics, goals, and stories created from them, stay in the domain where they were created. Domains outside that hierarchy can't see these records.
-   Product feedback submitted for an AI asset, and any demand created from that feedback, stay in the same domain as the asset. Domains outside that hierarchy can't access the related records.

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

