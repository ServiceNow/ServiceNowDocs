---
title: Agentic development in ServiceNow AI Platform environments
description: You can develop apps agentically with AI tools on the ServiceNow AI Platform in an isolated environment using a non-production instance with Developer Sandboxes, or on a Personal Developer Instance \(PDI\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/vibe-coding-environments.html
release: australia
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 3
keywords: [vibe coding, AI-assisted development, Developer Sandboxes, Personal Developer Instance, PDI, Build Agent, development environment, AI tools, non-production instance, isolated environment, parallel development, version control, Git workflows, metadata copy, ServiceNow SDK, VS Code]
breadcrumb: [Develop, Agentic development, Agentic development on the ServiceNow AI Platform, Building applications]
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

    Supports Git-based workflows for compliance and architectural standards. Update sets are also available.

-   **On-demand provisioning**

    Developer Sandboxes can be requested and provisioned on demand.


Use Developer Sandboxes to reduce change conflicts, enable branching and merging strategies, and reduce risk in enterprise-scale development.

Agentic development works with Developer Sandboxes in the following ways:

-   Agentic development accelerates app creation, while Developer Sandboxes provide an isolated space to experiment with AI-generated metadata changes.
-   You can track, preview, and roll back agentic changes in a sandbox to support governance and compliance.
-   Table data in a sandbox follows the configuration of each table. By default, tables use the Shared configuration, so records created on a Shared table are also available on the base instance and in other sandboxes that share the table. For more information, see [Developer Sandboxes and metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-metadata.md).
-   You must manually update incoming integrations to support the unique URLs of sandboxes. For more information, see [Supported ServiceNow AI Platform features in Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-supported-features.md).
-   Family, patch, and security upgrades retire existing sandboxes and recreate them. Restore changes from pre-existing sandboxes from the automatic backup, which is available only for instances beginning with Australia Patch 3. Save your work to source control or update sets consistently. For more information, see [Cloning and upgrading considerations for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.md).

For more information on Developer Sandboxes, see [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/sandboxes-landing.md).

## PDIs and agentic development

A Personal Developer Instance \(PDI\) is a free, standalone ServiceNow instance provided for personal use and experimentation. It is not connected to a customer’s production environment and is controlled by ServiceNow. PDIs are empty instances where developers set up apps and data from scratch.

-   The ServiceNow AI Platform offers Build Agent trials in PDIs with a limit of 25 prompts per 30-day cycle for personal experimentation.
-   Try out Build Agent on a PDI to experience agentic development without impacting production environments.
-   PDIs support learning prompting patterns, testing AI-generated apps, and refining workflows before moving to Developer Sandboxes or non-production instances.
-   For work that you plan to promote, use Developer Sandboxes on a non-production instance. Sandboxes start with the metadata of the base instance and support source control integration.

For more information on PDIs, see [Personal developer instance guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/personal_developer_instance_guide.md).

**Parent Topic:**[Agentic development on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/vibe-coding-using.md)

