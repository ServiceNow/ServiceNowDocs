---
title: Getting started with Build Agent
description: Use the following guidelines to help you transition from using App Engine Studio to Build Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/app-engine-studio/aes-getting-started-with-build-agent.html
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 4
keywords: [App Engine Studio, Get started with Build Agent, Switch to Build Agent, Migrate to Build Agent]
breadcrumb: [Migrating to Build Agent, Explore, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Getting started with Build Agent

Use the following guidelines to help you transition from using App Engine Studio to Build Agent.

## From wizard completion to intent-driven prompts

App Engine Studio \(AES\) development is a series of guided wizard steps that result in building an application and app files. Each step corresponds to a discrete decision, such as adding a table, adding a field, or configuring a form. The wizard interface constrains what you can do and sequences the choices for you.

With Build Agent, development occurs via a conversational interface. In either ServiceNow Studio or the ServiceNow IDE, you describe the application that you want, who it's for, and what it should contain. From that description, Build Agent produces the artifact. Unlike AES, the Build Agent interface doesn't constrain your choices. Instead, Build Agent interprets your intent and generates output accordingly.

This process means learning how to write prompts that are clear and effective. Prompts should lead with the purpose of the application and the key workflows it needs to support, rather than describing a request for a specific artifact. For guidance on effective prompting, see [General guidelines for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-general-guidelines.md) and [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-example-prompts.md).

## Owning the review step

With AES, the constraints imposed by the wizard interface meant that you were limited in what you could create accidentally. For example, you were unlikely to create apps or files that affect entire instance performance by accident.

However, with Build Agent, you have access to create the full set of artifacts available on the ServiceNow AI Platform. With this greater range of creation abilities, the necessity of reviewing your development output becomes of even greater importance and impact to your instance performance and security. So you must shift to owning the review step when migrating applications to Build Agent.

Before accepting any Build Agent output, read the generated code and description. Treat the output as a strong first draft that might not contain specific business rules, data volumes, or performance requirements for your organization.

The core workflow of prompting, reviewing, and accepting or rejecting is consistent across every Build Agent session. For more information, see [Build Agent workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-workflow.md).

## Iteration over prompt perfection

When creating apps and files in AES, modifying selections that you made during the creation process could sometimes prove to be difficult or require restarting the process entirely. But with Build Agent, the agent supports iteration by default. From prompt to prompt, Build Agent can process corrections and adjust the output accordingly. You can also create checkpoints with Build Agent, which help you distinguish one artifact version from another across sessions. For more information, see [Build Agent checkpoints and conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-conversational-change-log.md).

Prioritize iteration over a perfectly articulated prompt when developing with Build Agent. Attempting to write a single, catch-all prompt that describes an entire application and all of its artifacts rarely produces better results than the iterative approach. If needed, you can also revert your changes with Build Agent. For more information, see [Revert app changes with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/revert-app-changes-using-build-agent.md).

## Session continuity

Development in AES is stateless, meaning that each app a file you create is discrete and independent of the existence of other files. AES also doesn't store data about your work from one session to the next.

Build Agent accumulates information about your data model, business rules, and design decisions during each session. Sessions are then stored, enabling you to choose between rejoining an earlier session or starting a new one.

Learning how to structure your work between and across sessions is helpful when developing with Build Agent. Determine whether your work would benefit from the accumulated context of an existing session. For less complex builds or single artifact extensions, you can start a new session. For more information about sessions and limitations, see [Build Agent limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-limitations.md).

## Build Agent as a development partner

AES is a development tool. When you're ready to build an application or file, you enter the AES development environment and create or modify app files.

With Build Agent, you can use the chat panel as both a development tool and a design/planning partner. For example, you can use Build Agent to:

-   Brainstorm application architecture before writing any code
-   Analyze an existing AES application and identify where scripting or additional artifacts would improve it
-   Generate README documentation for an application
-   Add comments to existing scripts
-   Refine requirements before committing to a data model
-   Identify scope conflicts in applications that originated globally

These activities don't produce deployable artifacts on their own, but they can help to reduce the uncertainty that leads to rework. Using Build Agent to think through a build before prompting can result in higher quality output.

**Related topics**  


[Build Agent use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/additional-build-agent-use-cases.md)

