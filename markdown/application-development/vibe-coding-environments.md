---
title: Agentic development in ServiceNow AI Platform environments
description: You can develop apps agentically with AI tools on the ServiceNow AI Platform in an isolated environment using a non-production instance with Developer Sandboxes, or on a Personal Developer Instance \(PDI\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/vibe-coding-environments.html
release: brazil
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 4
keywords: [vibe coding, AI-assisted development, Developer Sandboxes, Personal Developer Instance, PDI, Build Agent, development environment, AI tools, non-production instance, isolated environment, parallel development, version control, Git workflows, metadata copy, ServiceNow SDK, VS Code]
breadcrumb: [Develop, Agentic development guide, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Agentic development in ServiceNow AI Platform environments

You can develop apps agentically with AI tools on the ServiceNow AI Platform in an isolated environment using a non-production instance with Developer Sandboxes, or on a Personal Developer Instance \(PDI\).

**Note:** You can develop for ServiceNow locally, outside of an instance using local VS Code and the ServiceNow SDK. However, this topic discusses agentic development on the ServiceNow AI Platform on an instance.

## Developer Sandboxes and development

Developer Sandboxes are isolated environments within a non-production instance that enable developers to build and test changes without impacting other work. They solve the problem of shared-instance conflicts by providing the following capabilities:

-   **Parallel development**

    Each sandbox is independent, so multiple developers can work concurrently.

-   **Full metadata copy**

    Developer Sandboxes start with the metadata of the base instance.

-   **Version control alignment**

    Supports Git-based workflows for compliance and architectural standards. Each sandbox inherits Git credentials from the base instance and can connect to source control with its own branch.Sandboxes work with legacy source control and the updated source control in ServiceNow Studio. Update sets are also available. For more information, see [Source control and Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sandboxes-source-control.md).

-   **On-demand provisioning**

    Developer Sandboxes can be requested and provisioned on demand.When you allocate a sandbox, you claim one from a pool of pre-created sandboxes instead of waiting for a new instance to be provisioned.Pooled sandboxes might be out of date with the current state of the base instance.


Use Developer Sandboxes to reduce change conflicts, enable branching and merging strategies, and reduce risk in enterprise-scale development.

Agentic development works with Developer Sandboxes in the following ways:

-   Agentic development accelerates app creation, while Developer Sandboxes provide an isolated space to experiment with AI-generated metadata changes.
-   You can track, preview, and roll back agentic changes in a sandbox to support governance and compliance.
-   Table data in a sandbox follows the configuration of each table. By default, tables use the Shared configuration, so records created on a Shared table are also available on the base instance and in other sandboxes that share the table. For more information, see [Developer Sandboxes and metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-metadata.md).
-   Sandboxes work best with ServiceNow Fluent and the ServiceNow IDE, which help avoid the merge issues that low-code XML changes can cause. For more information, see [General guidelines and use cases for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-general-guidelines.md).
-   Because each sandbox has a unique URL, you must manually update incoming integrations to support sandbox URLs. For more information, see [Supported ServiceNow AI Platform features in Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-supported-features.md).

Back up your work in a sandbox before you clone or upgrade an instance, either by exporting the update sets or committing to source control. For more information, see [Cloning and upgrading considerations for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.md).

For more information on Developer Sandboxes, see [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/sandboxes-landing.md).

## PDIs and agentic development

A Personal Developer Instance \(PDI\) is a free, standalone ServiceNow instance provided for personal use and experimentation. It is not connected to a customer’s production environment and is controlled by ServiceNow. PDIs are empty instances where developers set up apps and data from scratch.

-   The ServiceNow AI Platform offers Build Agent trials in PDIs with a limit of 25 prompts per user in a rolling 30-day period for personal experimentation.
-   Try out Build Agent on a PDI to experience agentic development without impacting production environments.
-   PDIs support learning prompting patterns, testing AI-generated apps, and refining workflows before moving to Developer Sandboxes or non-production instances.
-   For work that you plan to promote, use Developer Sandboxes on a non-production instance. Sandboxes start with the metadata of the base instance and support source control integration.

For more information on PDIs, see [Personal developer instance guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/personal_developer_instance_guide.md).

**Parent Topic:**[Agentic development on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/vibe-coding-using.md)

