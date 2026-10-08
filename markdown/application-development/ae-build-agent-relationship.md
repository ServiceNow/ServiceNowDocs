---
title: Autonomous Engineer and Build Agent
description: Autonomous Engineer and Build Agent are separate products that work together. Autonomous Engineer uses Build Agent as its execution layer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ae-build-agent-relationship.html
release: australia
topic_type: concept
last_updated: "2026-09-16"
reading_time_minutes: 3
keywords: [Autonomous Engineer, Build Agent, agentic development, ServiceNow Studio, agent packs, update sets]
audience: programmer
breadcrumb: [Overview, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Autonomous Engineer and Build Agent

Autonomous Engineer and Build Agent are separate products that work together. Autonomous Engineer uses Build Agent as its execution layer.

## Separate products

Autonomous Engineer and Build Agent are separately entitled products. Check your entitlements to determine your access to each. You can use Build Agent without Autonomous Engineer, but Autonomous Engineer requires Build Agent to run.

-   **Build Agent**

    An autonomous AI agent that creates and updates ServiceNow applications through a conversational chat interface in ServiceNow Studio and the ServiceNow IDE. You interact with Build Agent directly through natural language to build, edit, and deploy applications to update sets.

-   **Autonomous Engineer**

    An agentic worker that accepts requirements, generates a structured implementation plan, and builds all work items in parallel using background agents. Autonomous Engineer handles large or complex implementations where building each artifact manually is not practical. Autonomous Engineer is available in ServiceNow Studio.


**Note:** Autonomous Engineer is a separate application available in the ServiceNow Store. Installing Autonomous Engineer also installs Build Agent as a dependency. Installing Build Agent alone does not install Autonomous Engineer.

## How they work together

Autonomous Engineer uses Build Agent as its execution layer. When Autonomous Engineer builds work items in the execution phase, it does so through Build Agent. The Build Agent chat panel displays status updates and surfaces work items that require your review during execution.

Both products are available in ServiceNow Studio. You can use the Build Agent chat panel to interact with either product depending on your development needs. Use Build Agent for conversational, incremental development. Use Autonomous Engineer when you need to go from a full set of requirements to a complete implementation without building each artifact manually.

## What is shared

The following are shared between Autonomous Engineer and Build Agent:

-   **ServiceNow Studio environment**

    Both products run in ServiceNow Studio. The Explorer panel, editor tabs, and open files are in context for both products.

-   **Build Agent chat panel**

    The chat panel in ServiceNow Studio is the interface for both products. During an Autonomous Engineer run, the chat panel surfaces work items that need your attention and displays progress from background agents.

-   **Test Agent integration**

    Both products generate and run Test Agent tests as part of the build process to validate artifacts before deployment. For more information, see [Test what you built with Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-test-what-you-built.md).

-   **Tools**

    Both products use the same set of tools to support application development tasks such as semantic search, schema inspection, code search, UI validation, database querying, and script execution. For more information, see [Supported tools for Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-supported-tools.md).

-   **Models**

    Both products draw from the same set of supported AI models. You can change the active model from within either product. For more information, see [Supported models for Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-supported-models.md).

-   **Settings**

    Configuration settings for Autonomous Engineer and Build Agent are managed in the same location. Settings that apply to Build Agent also apply when Autonomous Engineer runs. For more information, see [Configure Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-autonomous-engineer.md).

-   **Deployment**

    Both products use the same deployment methods to move applications from development to production environments, including update sets and the application repository. For more information, see [Deploying what you built with Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-deployment.md).


**Parent Topic:**[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/exploring-autonomous-engineer.md)

