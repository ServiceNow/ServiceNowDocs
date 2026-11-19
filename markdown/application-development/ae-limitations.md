---
title: Autonomous Engineer limitations
description: Understand the constraints that apply to Autonomous Engineer before you build or deploy. Because Autonomous Engineer depends on Build Agent as its execution layer, limitations affecting Build Agent, including regulated environment restrictions and deployment constraints also apply.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-limitations.html
release: brazil
topic_type: concept
last_updated: "2026-11-10"
reading_time_minutes: 3
keywords: [Autonomous Engineer, limitations, constraints, Build Agent, regulated environments]
audience: programmer
breadcrumb: [Overview, Autonomous Engineer, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Autonomous Engineer limitations

Understand the constraints that apply to Autonomous Engineer before you build or deploy. Because Autonomous Engineer depends on Build Agent as its execution layer, limitations affecting Build Agent, including regulated environment restrictions and deployment constraints also apply.

Autonomous Engineer depends on Build Agent as its execution layer. Limitations that apply to Build Agent, including constraints on regulated environments, deployment capabilities, and performance, also apply when Autonomous Engineer runs.

## General limitations of Build Agent and Autonomous Engineer

Be aware of the following limitations when using Build Agent or Autonomous Engineer:

-   AI-generated code requires human review for ACL correctness, security, platform conventions, and governance compliance. Put peer-review gates, static checks, and validation steps in place.
-   You still must work with builders in ServiceNow Studio for app files and metadata types not yet supported in Build Agent or Autonomous Engineer, such as certain tables, UIs, or advanced features.

    **Note:** Build Agent and Autonomous Engineer can work on existing applications. You can use them to enhance base workflows, such as creating business rules on existing tables.

-   Security in apps developed with Build Agent or Autonomous Engineer is at the application and API level, not at granular record and field level by default. However, you can use agentic development to build security onto the app by making requests. For examples, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-example-prompts.md).
-   Limited support for cross-product AI integration.

Build Agent and Autonomous Engineer can generate data models and business rules. You should understand where data from your AI-generated apps is stored on the ServiceNow AI Platform.

## Build Agent, Autonomous Engineer, and ServiceNow Fluent

To understand the upper limit of what Build Agent and Autonomous Engineer can do, review the ServiceNow Fluent documentation. If you're not familiar with the ServiceNow AI Platform, the ServiceNow Fluent documentation can help you determine what they can do. For more information, see the following topics:

-   [ServiceNow Fluent API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-sdk/servicenow-fluent-api-reference.md)
-   [ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-fluent.md)

If ServiceNow Fluent does not support a metadata type, Build Agent and Autonomous Engineer cannot update it unless you provide precise platform-specific instructions.

## Regulated environments

Build Agent, Autonomous Engineer, and Test Agent depend on off-instance services that have not completed the security compliance review required for regulated hosting environments. As a result, Build Agent v2 \(Australia Patch 0 and Zurich 8 and higher\) is not available in GCC, NSC, or FedRAMP environments.

**Note:** As of Brazil Patch 1, Build Agent, Autonomous Engineer, and Test Agent support ServiceNow Protected Platform \(SPP\) for Australia, the EU, and Singapore.

Customers in regulated environments must remain on Build Agent v1, which runs on-platform and is certified for regulated use.Autonomous Engineer, which depends on Build Agent v2 services, is also unavailable in regulated environments.

In regulated environments where Build Agent v2 is unavailable, you can continue to use the following:

-   Core update set and Git workflows in ServiceNow Studio.
-   Instance Scan

## Feedback on Autonomous Engineer

To give feedback on Autonomous Engineer, see the [Idea portal on Now Support](https://support.servicenow.com/ideas).

**Parent Topic:**[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-autonomous-engineer.md)

