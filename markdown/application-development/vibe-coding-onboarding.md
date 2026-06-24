---
title: Onboarding for agentic development
description: The following checklist helps to ensure your environment is properly configured, that you understand the core tools and general guidelines, and that you adopt secure, compliant workflows. Whether you're new to ServiceNow or transitioning to agentic development, this resource will set you up for success.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/vibe-coding-onboarding.html
release: zurich
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [Agentic development, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Onboarding for agentic development

The following checklist helps to ensure your environment is properly configured, that you understand the core tools and general guidelines, and that you adopt secure, compliant workflows. Whether you're new to ServiceNow or transitioning to agentic development, this resource will set you up for success.

## Agentic development access and setup

1.  Ensure you have credentials for the development instance.
2.  Confirm that you have the appropriate license for the tools you want to use, for example for Build Agent or Now Assist for Creator.
3.  Confirm that the plugins for the tools that you want to use are installed and activated. For more information, see the following topics:
    -   [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/install-build-agent.md)

        **Note:** You can also connect a Figma MCP server to Build Agent to accelerate the conversion of Figma designs into enterprise-grade applications. For more information, see [Connect Build Agent to a Figma MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/connect-figma-mcp-server-to-build-agent.md).

    -   [Install Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/now-assist-for-creator/install-now-assist-for-creator.md)
4.  Install Developer Sandboxes, which is not required for agentic development but provides a helpful instance to experiment with development. For more information, see [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/developer-sandboxes/sandboxes-landing.md).

ServiceNow Studio and ServiceNow IDE are automatically available on every instance, so you don't need to confirm their installation.

## Prepare your development environment

1.  Use Developer Sandboxes to allocate a sandbox for safe, isolated agentic development. For more information, see [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/developer-sandboxes/sandboxes-landing.md).
2.  Validate compliance policies and security controls.
3.  Enable Vault Console and Machine Identity Console for sensitive data protection and API governance.

## Learn core features

1.  Practice converting natural language prompts into apps using Build Agent.
2.  If you're using Now Assist for Creator tools, familiarize yourself with the following:
    -   Text-to-form/App scaffolding
    -   Code explanation and refactoring, though Build Agent has a more robust implementation.
3.  Explore multi-turn chat for iterative development through conversational prompting.

Visit the [App Engine Academy playlist on YouTube](https://www.youtube.com/playlist?list=PLkGSnjw5y2U4Td38CczvfDKxhcOuwg4CC) for recordings of training sessions.

## Get familiar with general guidelines

See [General guidelines for agentic development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/vibe-cooding-guidelines.md) for more information.

## Engage with the development community

Check out [ServiceNow Community](https://www.servicenow.com/community/) to connect with other developers and share ideas.

