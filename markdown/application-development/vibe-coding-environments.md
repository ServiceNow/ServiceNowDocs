---
title: Agentic development in ServiceNow AI Platform environments
description: You can develop apps agentically with AI tools on the ServiceNow AI Platform in a safe, isolated environment using a non-production instance with Developer Sandboxes, or on a Personal Developer Instance \(PDI\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/vibe-coding-environments.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [vibe coding, AI-assisted development, Developer Sandboxes, Personal Developer Instance, PDI, Build Agent, development environment, AI tools, non-production instance, isolated environment, parallel development, version control, Git workflows, metadata copy, ServiceNow SDK, VS Code]
breadcrumb: [Develop, Agentic development, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Agentic development in ServiceNow AI Platform environments

You can develop apps agentically with AI tools on the ServiceNow AI Platform in a safe, isolated environment using a non-production instance with Developer Sandboxes, or on a Personal Developer Instance \(PDI\).

**Note:** You can develop for ServiceNow locally, outside of an instance using local VS Code and the ServiceNow SDK. However, this topic discusses agentic development on the ServiceNow AI Platform on an instance.

## Developer Sandboxes and development

Developer Sandboxes are isolated environments within a non-production instance that enable developers to build and test changes without impacting other work. They solve the problem of shared-instance conflicts by providing the following capabilities:

-   **Parallel development**

    Each sandbox is independent, so multiple developers can work concurrently.

-   **Full metadata copy**

    Developer Sandboxes are initialized with the base instance's metadata.

-   **Version control alignment**

    Supports Git-based workflows for compliance and architectural standards. Update sets are also available.

-   **On-demand provisioning**

    Developer Sandboxes can be requested and spun up dynamically.


Use Developer Sandboxes to eliminate change conflicts, enable branching and merging strategies, and reduce risk in enterprise-scale development.

Agentic development works with Developer Sandboxes in the following ways:

-   Agentic development accelerates app creation, while Developer Sandboxes provide a safe space to experiment with AI-generated changes.
-   Every AI-assisted change in a sandbox can be tracked, previewed, and rolled back to maintain governance and compliance.

For more information on Developer Sandboxes, see [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/developer-sandboxes/sandboxes-landing.md).

## PDIs and AI-assisted development

A Personal Developer Instance \(PDI\) is a free, standalone ServiceNow instance provided for personal use and experimentation. It is not connected to a customer’s production environment and is controlled by ServiceNow. PDIs are empty instances where developers set up apps and data from scratch.

-   The ServiceNow AI Platform offers Build Agent trials in PDIs with a 10-prompt limit per month for personal experimentation.
-   Try out Build Agent on a PDI to experience agentic development without impacting production environments.
-   PDIs support learning prompting patterns, testing AI-generated apps, and refining workflows before moving to Developer Sandboxes or sub-production instances.
-   For production-grade work, use Developer Sandboxes instead, which are exact copies of customer instances and support source control integration.

For more information on PDIs, see [Personal developer instance guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/personal_developer_instance_guide.md).

**Parent Topic:**[Agentic development on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/vibe-coding-using.md)

