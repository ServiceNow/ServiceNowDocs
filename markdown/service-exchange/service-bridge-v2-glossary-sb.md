---
title: Service Exchange glossary
description: A list of terms used in Service Exchange.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
breadcrumb: [Reference, Service Exchange]
---

# Service Exchange glossary

A list of terms used in Service Exchange.

## A

Glossary terms are grouped alphabetically.

### application scope

A unique namespace and a set of permissions to access application files and data. Admins can specify the data that is accessible to other applications from the application record or from each table record.

### attachment sync

A feature that synchronizes file attachments between provider and consumer instances, ensuring both parties have access to attachments.

### authorized user

An individual user record that is permitted to access Service Exchange instances, as defined by the admins.

**Related topics**  


[Add an authorized user](../task/service-bridge-v2-create-auth-user.md)

## B

Glossary terms are grouped alphabetically.

### bi-directional integration

A connection that enables data and updates to flow both ways between provider and consumer Service Exchange instances to keep linked records in sync.

## C

Glossary terms are grouped alphabetically.

### consumer

A person or an organization that receives services from a provider through Service Exchange.

**Related topics**  


[Service Exchange for Consumers](../concept/service-bridge-consumers-landing-page.md)

### consumer application

A Service Exchange component installed on the consumer's instance that enables users to request services, track fulfillment, and exchange updates with their provider.

**Related topics**  


[Components installed with Service Exchange for Consumers](service-bridge-v2-installed-components-customer.md)

### consumer criteria

A filter criteria that determine which consumers are entitled to specific Service Exchange content, such as catalog items or tasks.

**Related topics**  


[Create a consumer criteria](../concept/service-bridge-v2-create-consumer-criteria.md)

### configuration revision

A versioned update to various [entitlements](service-bridge-v2-glossary-sb.md#), such as a remote record producer, remote task definition, or FDS offering, which enables providers to introduce new features without disrupting existing consumer entitlements.

**Related topics**  


[Configuring revisions](../concept/service-bridge-v2-config-revision.md)

## D

Glossary terms are grouped alphabetically.

### domain separation

A process to separate data, processes, and administrative tasks into logical groupings called domains. Admins can then control the information available to each domain, including which users can see and access the data. Typically used only in Multiple Service Provider \(MSP\) organizations.

**Related topics**  


[Domain separation and Service Exchange](service-bridge-v2-domain-separation.md)

## E

Glossary terms are grouped alphabetically.

### entitlement

A configuration mechanism in Service Exchange that determines which remote content, such as catalog items, record producers, remote tasks definitions, a consumer instance is allowed to access.

**Related topics**  


[Creating entitlements in Service Exchange for Providers](../concept/service-bridge-v2-entitlements.md)

## F

Glossary terms are grouped alphabetically.

### flow action

A predefined automation step in Workflow Studio that helps manage repetitive tasks in Service Exchange.

**Related topics**  


[Flow action](../concept/service-bridge-v2-flow-action.md)

### foundation data sync

A mechanism for scheduled, structured synchronization of foundational data \(such as assets, users, or locations\) from provider to consumer instances.

**Related topics**  


[Foundation data sync](../concept/service-bridge-v2-explore-foundation-data-sync.md)

## H

Glossary terms are grouped alphabetically.

### health dashboard

A centralized UI that displays health of connected instances, the results of system health checks, errors, and scan statuses in Service Exchange.

**Related topics**  


[Service Exchange Center](../concept/se-se-center.md)

## I

Glossary terms are grouped alphabetically.

### instance scan checks

Automated tests that identify configuration issues or system inconsistencies in Service Exchange to help administrators maintain system health and reduce downtime.

**Related topics**  


[Instance scan checks](../concept/service-bridge-v2-scan-checks.md)

[List of scan checks](service-bridge-v2-list-of-scan-checks-in-sb.md)

## J

Glossary terms are grouped alphabetically.

### Journal Field Framework

A framework that synchronizes journal-type fields, such as comments and work notes, between provider and consumer instances, preserving operational history and user attribution.

**Related topics**  


[Journal field frameworks](../concept/service-bridge-v2-expolre-journal-field-framework.md)

## K

Glossary terms are grouped alphabetically.

## L

Glossary terms are grouped alphabetically.

## M

Glossary terms are grouped alphabetically.

### magic link

A special URL that allows a consumer user to access a resource in the provider instance directly, bypassing manual login for a seamless experience.

**Related topics**  


[Magic links](../concept/service-bridge-v2-explore-magic-link.md)

## N

Glossary terms are grouped alphabetically.

## P

Glossary terms are grouped alphabetically.

### Partner

A person or an organization that supports service fulfillment on behalf of a provider, so a partner is essentially a provider for the provider's. Providers can delegate specific tasks to fulfillment partners, who operate within the same Service Exchange infrastructure. These partners receive, update, and complete tasks in real time, ensuring transparency, continuity, and coordinated service delivery across all participating parties.

### persona

A category used to define entitlement to catalog items or services by grouping authorized users.

**Related topics**  


[User roles for providers](../concept/service-bridge-v2-personas.md)

### proactive case

A case automatically generated to proactively notify and address impacted customers before they report an issue.

**Related topics**  


[Proactive cases](../concept/service-bridge-v2-proactive-case.md)

### provider

An organization or instance that offers and fulfills services for consumers using Service Exchange.

**Related topics**  


[Service Exchange for Providers](../concept/service-bridge-providers-landing-page.md)

### provider application

The Service Exchange component installed on the service provider's instance. It allows providers to publish service catalogs, manage requests, and fulfill tasks for consumers.

**Related topics**  


[Components installed with Service Exchange for Providers](service-bridge-v2-installed-components-provider.md)

### provider task

A task created in the provider instance to fulfill a consumer request, with status and updates synchronized to the consumer instance.

**Related topics**  


[Provider tasks](../concept/service-bridge-v2-provider-tasks.md)

## R

Glossary terms are grouped alphabetically.

### registration task

A task record initiates and monitors the status of a secure, bi-directional connection between provider and consumer instances, typically initiated by the provider.

### remote catalog

A catalog of services created by the provider and made available to consumers as catalog items in their own instance.

**Related topics**  


[Create remote catalogs in Service Exchange for providers](../concept/service-bridge-v2-remote-catalog.md)

### remote record producer

A configuration record that defines variables and inputs a consumer must provide to submit a request. When used, it creates a [provider task](service-bridge-v2-glossary-sb.md#) on the provider instance and triggers the appropriate fulfillment action. Task updates remain visible in both the provider and consumer instances throughout the process.

Also know as RRP.

**Related topics**  


[Remote record producers in Service Exchange](../concept/service-bridge-v2-remote-record.md)

### remote task

A linked task that enables synchronization of incidents, cases, or service requests between provider and consumer instances.

**Related topics**  


[Remote tasks](../concept/service-bridge-v2-remote-task-overview.md)

### role

A category assigned to a group or user to grant access to specific privileges in Service Exchange.

**Related topics**  


[User roles for providers](../concept/service-bridge-v2-personas.md)

## S

Glossary terms are grouped alphabetically.

### scratchpad

A feature that allows providers and consumers to exchange additional structured data \(name-value pairs\) associated with tasks, synchronized automatically between instances.

**Related topics**  


[Using the Scratchpad for Service Exchange tasks](../concept/service-bridge-v2-scratchpad.md)

### Service Exchange

An application that connects multiple ServiceNow instances \(provider, consumer, partner\) to enable seamless, bi-directional service delivery, collaboration, and data synchronization across organizational boundaries.

**Related topics**  


[Exploring Service Exchange](../concept/service-bridge-v2-exploring-service-bridge.md)

## T

Glossary terms are grouped alphabetically.

### transform framework

A tool for mapping and converting data between provider and consumer instances during remote task synchronization in Service Exchange. Transforms can be created once and reused across all remote task definitions.

**Related topics**  


[Transform data with the Service Exchange transform framework](../concept/service-bridge-v2-transform-about.md)

## V

Glossary terms are grouped alphabetically.

### variable

A form field that collects user input data in catalog items or remote record producers. Variables define the type, format, and validation rules for the information users provide when submitting service requests.

### variable set

A modular collection of variables that can be reused across multiple remote record producers to ensure consistency in data collection.

