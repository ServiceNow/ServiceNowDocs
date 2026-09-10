---
title: Migrating to Build Agent
description: Build Agent is the agentic development experience on the ServiceNow AI Platform. Migrate your applications from App Engine Studio to Build Agent to expand your app's capabilities and take advantage of the agentic developer experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-studio/aes-migrating-to-build-agent.html
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 3
keywords: [Migrate to Build Agent, AES to Build Agent, Build Agent, App Engine Studio, Agentic development]
breadcrumb: [Explore, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Migrating to Build Agent

Build Agent is the agentic development experience on the ServiceNow AI Platform. Migrate your applications from App Engine Studio to Build Agent to expand your app's capabilities and take advantage of the agentic developer experience.

## When to migrate to Build Agent

When building apps with App Engine Studio \(AES\), you may reach a point where your development needs exceed the scope of what AES can offer. You might need to add custom logic to an app, add scripting, or build global apps instead of scoped ones. When this occurs, you need to migrate your application to a development environment that supports more complex capabilities. Build Agent, the agentic developer experience on the ServiceNow AI Platform, supports these advanced capabilities, and the process of migrating apps to Build Agent happens in the background.

Build Agent is embedded within the same development environments \(ServiceNow Studio and the ServiceNow IDE\) that AES you already use when your work exceeds AES capabilities. The agent generates full-stack applications and artifacts using natural language prompts. To learn more about Build Agent, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent.md).

Whether you have an AES app that you want to extend, or you want to build something new, Build Agent offers the full suite of developer tools and the agentic development experience on the ServiceNow AI Platform.

## What migration involves

Migrating to Build Agent is more of a development workflow adjustment than an actual migration process. When you're ready to migrate to Build Agent, the agent converts [the the AES app to ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/convert-app-to-fluent.md), enabling you to work in an integrated development environment \(IDE\). When your app is converted to ServiceNow Fluent, you can also work in ServiceNow Studio. Existing applications and app artifacts, such as tables, flows, workspaces, ACLs, and playbooks, are already accessible in ServiceNow Studio and available to be modified with Build Agent.

What does change is how you complete tasks. AES developers are accustomed to thinking in terms of wizard steps and form completion, which guides them through completing specific tasks. Development using Build Agent, however, operates using natural language prompts and iterative development. So if you plan to migrate to Build Agent, you must adjust to the cycle of prompting, reviewing, and accepting or rejecting Build Agent output.

You also gain access to scripting, global scope applications, and modification of base system applications with Build Agent. For some, this might mean learning new systems or developing new practices for a different scale of work. For more information about adjusting to the Build Agent development workflow, see [Getting started with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-getting-started-with-build-agent.md).

## Key differences between App Engine Studio and Build Agent

In addition to the workflow adjustment, there are several differences between AES and Build Agent that affect the developer experience.

-   **Interface**

    AES uses a guided wizard interface, while Build Agent uses a conversational prompt interface inside ServiceNow Studio or the ServiceNow IDE.

-   **Scope**

    AES supports scoped applications only and creates only the artifacts enabled by its integrated builders, such as tables, experiences, flows, workspaces, and ACLs. Build Agent supports scoped and global applications and can create the full set of development artifacts, including business rules, Script Includes, Client Scripts, ACLs, and UI Builder pages.

-   **Script access**

    To add scripting to AES applications, you must convert the application to ServiceNow Fluent and open the application in an IDE, such as ServiceNow Studio. Because Build Agent is already embedded within an IDE, the agent generates and modifies scripts.

-   **Base system application modification**

    With AES, you can modify only custom, scoped applications. Build Agent supports the modification of any application, including base system applications.


For a full side-by-side comparison between App Engine Studio and Build Agent, see [App Engine Studio and Build Agent feature comparison](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-vs-ba-feature-comparison.md).

