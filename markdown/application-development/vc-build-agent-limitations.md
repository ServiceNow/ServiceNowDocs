---
title: Limitations of AI-assisted app generation with Build Agent
description: Build Agent accelerates AI-assisted app development, but it also has some limitations that you should understand before using it. These constraints span feature coverage, platform compatibility, and governance requirements, all of which affect how and when you can use the tool effectively in vibe coding workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build Agent overview, Develop, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Limitations of AI-assisted app generation with Build Agent

Build Agent accelerates AI-assisted app development, but it also has some limitations that you should understand before using it. These constraints span feature coverage, platform compatibility, and governance requirements, all of which affect how and when you can use the tool effectively in vibe coding workflows.

## General limitations of Build Agent

Be aware of the following limitations when using Build Agent:

-   AI-generated code requires human review for ACL correctness, security, platform conventions, and governance compliance. Put peer-review gates, static checks, and validation steps in place.
-   You still need to work with builders in ServiceNow Studio for app files and metadata types not yet supported in Build Agent, such as certain tables, UIs, or advanced features.

    **Note:** Build Agent can work on existing applications. You can use Build Agent to enhance base workflows, such as creating business rules on existing tables.

-   Security in apps developed with Build Agent is at the application and API level, not at granular record and field level by default. However, you can vibe code security onto the app by making requests. For examples, see [Example prompts for vibe coding and AI-assisted development](../reference/vibe-coding-example-prompts.md).
-   Limited support for cross-product AI integration.

Build Agent can generate data models and business rules. You should understand where data from your AI-generated apps is stored on the ServiceNow AI Platform.

## Build Agent and ServiceNow Fluent

To understand the upper limit of what Build Agent can do, review the ServiceNow Fluent documentation. If you are not familiar with the ServiceNow AI Platform, the ServiceNow Fluent documentation can help you determine what Build Agent can do. For more information, see the following topics:

-   [ServiceNow Fluent API reference](../../servicenow-sdk/reference/servicenow-fluent-api-reference.md)
-   [ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md)

If there isn't a mapping between ServiceNow Fluent and the XML metadata, then Build Agent can't update the data unless you understand the platform well enough to precisely instruct Build Agent to make the changes you need.

**Parent Topic:**[AI-assisted ServiceNow AI Platform development with Build Agent](vc-build-agent-landing.md)

