---
title: Build Agent limitations
description: Plan deployments and troubleshoot issues by learning about Build Agent constraints that affect deployment capabilities and performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/build-agent-limitations.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Build Agent limitations

Plan deployments and troubleshoot issues by learning about Build Agent constraints that affect deployment capabilities and performance.

## Troubleshooting

If you encounter something that Build Agent can't currently do, complete that step directly on the ServiceNow AI Platform® and keep working with Build Agent for the rest of your development. Build Agent is designed to complement your workflow, not to replace it.

For details on troubleshooting, see [Common issues and solutions in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/build-agent-troubleshooting.md).

## General limitations of Build Agent

Be aware of the following limitations when using Build Agent:

-   AI-generated code requires human review for ACL correctness, security, platform conventions, and governance compliance. Put peer-review gates, static checks, and validation steps in place.
-   You still must work with builders in ServiceNow Studio for app files and metadata types not yet supported in Build Agent, such as certain tables, UIs, or advanced features.

    **Note:** Build Agent can work on existing applications. You can use Build Agent to enhance base workflows, such as creating business rules on existing tables.

-   Security in apps developed with Build Agent is at the application and API level, not at granular record and field level by default. However, you can vibe code security onto the app by making requests. For examples, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/build-agent-example-prompts.md).
-   Limited support for cross-product AI integration.

Build Agent can generate data models and business rules. You should understand where data from your AI-generated apps is stored on the ServiceNow AI Platform.

## Build Agent and ServiceNow Fluent

To understand the upper limit of what Build Agent can do, review the ServiceNow Fluent documentation. If you're not familiar with the ServiceNow AI Platform, the ServiceNow Fluent documentation can help you determine what Build Agent can do. For more information, see the following topics:

-   [ServiceNow Fluent API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-sdk/servicenow-fluent-api-reference.md)
-   [ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/servicenow-fluent.md)

If there isn't a mapping between ServiceNow Fluent and the XML metadata, then Build Agent can't update the data unless you understand the platform well enough to precisely instruct Build Agent to make the changes you need.

## Feedback on Build Agent

To give feedback on Build Agent, see the [Idea portal on Now Support](https://support.servicenow.com/ideas).

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/exploring-build-agent.md)

