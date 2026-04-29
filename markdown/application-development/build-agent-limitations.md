---
title: Build Agent limitations
description: Plan deployments and troubleshoot issues by understanding Build Agent constraints that affect deployment capabilities and performance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 2
breadcrumb: [Explore, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Build Agent limitations

Plan deployments and troubleshoot issues by understanding Build Agent constraints that affect deployment capabilities and performance.

## General limitations of Build Agent

Be aware of the following limitations when using Build Agent:

-   AI-generated code requires human review for ACL correctness, security, platform conventions, and governance compliance. Put peer-review gates, static checks, and validation steps in place.
-   You still need to work with builders in ServiceNow Studio for app files and metadata types not yet supported in Build Agent, such as certain tables, UIs, or advanced features.

    **Note:** Build Agent can work on existing applications. You can use Build Agent to enhance base workflows, such as creating business rules on existing tables.

-   Security in apps developed with Build Agent is at the application and API level, not at granular record and field level by default. However, you can vibe code security onto the app by making requests. For examples, see [Example prompts for vibe coding and AI-assisted development](../../vibe-coding/reference/vibe-coding-example-prompts.md).
-   Limited support for cross-product AI integration.

Build Agent can generate data models and business rules. You should understand where data from your AI-generated apps is stored on the ServiceNow AI Platform.

## Build Agent and ServiceNow Fluent

To understand the upper limit of what Build Agent can do, review the ServiceNow Fluent documentation. If you are not familiar with the ServiceNow AI Platform, the ServiceNow Fluent documentation can help you determine what Build Agent can do. For more information, see the following topics:

-   [ServiceNow Fluent API reference](../../servicenow-sdk/reference/servicenow-fluent-api-reference.md)
-   [ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md)

If there isn't a mapping between ServiceNow Fluent and the XML metadata, then Build Agent can't update the data unless you understand the platform well enough to precisely instruct Build Agent to make the changes you need.

## Troubleshooting

For details on troubleshooting, see [Troubleshooting in Build Agent](../reference/build-agent-troubleshooting.md).

**Parent Topic:**[Exploring Build Agent](exploring-build-agent.md)

