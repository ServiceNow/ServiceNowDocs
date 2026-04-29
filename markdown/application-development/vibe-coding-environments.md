---
title: Vibe coding and AI-assisted development in ServiceNow AI Platform environments
description: You can vibe code and develop apps with AI tools on the ServiceNow AI Platform in a safe, isolated environment using a non-production instance with Developer Sandboxes, or on a Personal Developer Instance \(PDI\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [vibe coding, AI-assisted development, Developer Sandboxes, Personal Developer Instance, PDI, Build Agent, development environment, AI tools, non-production instance, isolated environment, parallel development, version control, Git workflows, metadata copy, ServiceNow SDK, VS Code]
breadcrumb: [Develop, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Vibe coding and AI-assisted development in ServiceNow AI Platform environments

You can vibe code and develop apps with AI tools on the ServiceNow AI Platform in a safe, isolated environment using a non-production instance with Developer Sandboxes, or on a Personal Developer Instance \(PDI\).

**Note:** You can develop for ServiceNow locally, outside of an instance using local VS Code and the ServiceNow SDK. However, this topic discusses vibe coding and AI-assisted development on the ServiceNow AI Platform on an instance.

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

Vibe coding and AI-assisted development works with Developer Sandboxes in the following ways:

-   Vibe coding accelerates app creation, while Developer Sandboxes provide a safe space to experiment with AI-generated changes.
-   Every AI-assisted change in a sandbox can be tracked, previewed, and rolled back to maintain governance and compliance.

For more information on Developer Sandboxes, see [Developer Sandboxes](../../developer-sandboxes/concept/sandboxes-landing.md).

## PDIs and AI-assisted development

A Personal Developer Instance \(PDI\) is a free, standalone ServiceNow instance provided for personal use and experimentation. It is not connected to a customer’s production environment and is controlled by ServiceNow. PDIs are empty instances where developers set up apps and data from scratch.

-   The ServiceNow AI Platform offers Build Agent trials in PDIs with a 10-prompt limit per month for personal experimentation.
-   Try out Build Agent on a PDI to experience vibe coding and AI-assisted development without impacting production environments.
-   PDIs support learning prompting patterns, testing AI-generated apps, and refining workflows before moving to Developer Sandboxes or sub-production instances.
-   For production-grade work, use Developer Sandboxes instead, which are exact copies of customer instances and support source control integration.

For more information on PDIs, see [Personal developer instance guide](../../applications/concept/personal_developer_instance_guide.md).

**Parent Topic:**[Vibe coding and AI-assisted development on the ServiceNow AI Platform](vibe-coding-using.md)

