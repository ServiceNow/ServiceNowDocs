---
title: Playbook authoring with Build Agent
description: Use Build Agent to author and manage Playbook Designer artifacts through a conversation. You can generate playbook structures, configure activities, set runtime permissions, and define launcher configurations without manually navigating the Playbook Designer UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ba-playbooks.html
release: zurich
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 2
keywords: [playbook, playbook authoring, build agent playbook, playbook designer, fluent playbook, playbook launcher, runtime permissions, ServiceNow Otto, AI Agents, generative AI, agentic AI]
audience: developer
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Playbook authoring with Build Agent

Use Build Agent to author and manage Playbook Designer artifacts through a conversation. You can generate playbook structures, configure activities, set runtime permissions, and define launcher configurations without manually navigating the Playbook Designer UI.

Build Agent can generate and configure Playbook Designer artifacts from a conversation. Describe the playbook structure, activity logic, or configuration you need, and Build Agent produces the corresponding records and settings on your instance.

For more information on playbooks, see [Exploring Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer.md).

## Fluent-based playbook authoring

You can build, edit, and manage Platform Playbooks using the Fluent TypeScript DSL directly in the ServiceNow IDE or a local SDK. Playbook components such as stages, triggers, and roles are defined as modular `.ts` files that support Git-based version control and team collaboration.

Existing playbooks can be converted to Fluent format. During conversion, metadata is transformed into editable and deployable `.ts` files. Use `now-sdk fetch` and `now-sdk deploy` commands to sync playbook changes bidirectionally between a local IDE and a ServiceNow instance.

All playbook records related to a playbook definition are consolidated into a single XML update set file, which simplifies version control and deployment.

## What you can do from chat

From the Build Agent chat panel, you can:

-   Generate playbook structures including stages, activities, and conditions
-   Generate runtime permissions at the playbook level and at the stage level
-   Generate and configure the Set Playbook Outputs activity for nested playbooks
-   Configure agentic fields on form-based and record-based activities when the AI Agent plugin is active
-   Generate on-demand playbook launcher configurations
-   Configure golden path settings and define the ideal path through decision nodes.
-   Author public playbooks and playbook variants
-   Configure Go back to activity definitions
-   Configure golden path settings
-   Use Automation plan pills in playbook activities
-   Generate playbook scaffolding from an uploaded image

## Considerations for playbooks

-   Agentic activity field configuration requires the AI Agent plugin to be active on your instance.
-   Fluent-based playbook authoring requires ServiceNow IDE or the ServiceNow SDK.
-   For supported playbook metadata types, see [Supported metadata in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-supported-metadata.md).

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/exploring-build-agent.md)

