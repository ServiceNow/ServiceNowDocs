---
title: Limitations of agentic app generation with Build Agent
description: Build Agent accelerates agentic app development, but it also has some limitations that you should understand before using it. These constraints span feature coverage, platform compatibility, and governance requirements, all of which affect how and when you can use the tool effectively in agentic development workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/vc-build-agent-limitations.html
release: australia
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 2
breadcrumb: [Build Agent overview, Develop, Agentic development, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Limitations of agentic app generation with Build Agent

Build Agent accelerates agentic app development, but it also has some limitations that you should understand before using it. These constraints span feature coverage, platform compatibility, and governance requirements, all of which affect how and when you can use the tool effectively in agentic development workflows.

## General limitations of Build Agent

Be aware of the following limitations when using Build Agent:

-   AI-generated code requires human review for ACL correctness, security, platform conventions, and governance compliance. Put peer-review gates, static checks, and validation steps in place.
-   You still must work with builders in ServiceNow Studio for app files and metadata types not yet supported in Build Agent, such as certain tables, UIs, or advanced features.

    **Note:** Build Agent can work on existing applications. You can use Build Agent to enhance base workflows, such as creating business rules on existing tables.

-   Security in apps developed with Build Agent is at the application and API level, not at granular record and field level by default. However, you can use agentic development to build security onto the app by making requests. For examples, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-example-prompts.md).
-   Limited support for cross-product AI integration.

Build Agent can generate data models and business rules. You should understand where data from your AI-generated apps is stored on the ServiceNow AI Platform.

## Build Agent and ServiceNow Fluent

To understand the upper limit of what Build Agent can do, review the ServiceNow Fluent documentation. If you're not familiar with the ServiceNow AI Platform, the ServiceNow Fluent documentation can help you determine what Build Agent can do. For more information, see the following topics:

-   [ServiceNow Fluent API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-sdk/servicenow-fluent-api-reference.md)
-   [ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-fluent.md)

If ServiceNow Fluent does not support a metadata type, Build Agent cannot update it unless you provide precise platform-specific instructions.

## Regulated environments

Build Agent, Autonomous Engineer, and Test Agent depend on off-instance services that haven't completed the security compliance review required for regulated hosting environments. As a result, Build Agent v2, which begins with Australia Patch 0 and Zurich 8, isn't available in GCC, NSC, or FedRAMP environments.

**Note:** As of Australia Patch 6, Build Agent, Autonomous Engineer, and Test Agent support ServiceNow Protected Platform for Australia, the EU, and Singapore.

For the options that are available in regulated environments, see [Build Agent limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-limitations.md).

## Limitations of Autonomous Engineer

Limitations that apply to Build Agent also apply to Autonomous Engineer. For more information, see [Autonomous Engineer limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-limitations.md).

**Parent Topic:**[Agentic ServiceNow AI Platform development with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/vc-build-agent-landing.md)

