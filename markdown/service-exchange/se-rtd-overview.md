---
title: Remote task definition
description: A remote task definition \(RTD\) is the provider-side configuration that determines how tasks synchronize between a provider and consumer instance in Service Exchange. It defines the linked tables, the field mappings, and the consumer entitlements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-rtd-overview.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 2
breadcrumb: [Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Remote task definition

A remote task definition \(RTD\) is the provider-side configuration that determines how tasks synchronize between a provider and consumer instance in Service Exchange. It defines the linked tables, the field mappings, and the consumer entitlements.

An RTD doesn't represent an actual piece of work. It is the reusable blueprint that a remote task is created from whenever an incident, case, or service request needs to synchronize between the provider and consumer instances.

## What an RTD defines

An RTD links one provider table and one consumer table, for example Case to Incident, and specifies the following information.

-   Inbound fields: data the provider receives from the consumer when a remote task is created or updated.
-   Outbound fields: data the provider sends to the consumer.
-   Virtual fields: fields that exist on one side's table but not the other. Since there's no matching field to map to, the value comes from a transform instead of a direct mapping.
-   Consumer criteria: which consumers are entitled to use this RTD.

When the RTD is published, the system automatically generates remote task variables from the inbound fields. These variables render on the actual remote task form.

## Lifecycle

A remote task definition moves through Draft, Published, Inactive, Archived, and Retired states. Publishing entitles the RTD to matching consumers. You can revise a published RTD through a configuration revision. Checking out an RTD creates a new Draft version. When you publish that version, the system moves the previous version to Inactive rather than removing it. This ensures existing consumers continue working until they explicitly upgrade.

The following table lists the tasks for creating an RTD and for creating a remote task from a RTD.

|Link|Created in|Description|
|----|----------|-----------|
|[Create a remote task definition in Service Exchange for Providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-create-remote-tasks-defs.md)|Service Exchange|An administrator selects the provider and consumer tables directly, then maps each inbound and outbound field manually.|
|[Create a remote task definition with AI assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/create-remote-task-definition-ai-assistance.md)|Service Exchange|An administrator describes the tables to ServiceNow Otto, which generates the field mappings automatically for review before publishing.|
|[Create a remote task using Workflow Studio in Service Exchange for Providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-create-remote-task-flow-desig.md)|Workflow Studio|A flow, built once, creates a remote task automatically from a published RTD whenever its trigger condition is met.|

