---
title: Agentic development on the ServiceNow AI Platform
description: Build and enhance custom applications using the generative and agentic AI capabilities available on the ServiceNow AI Platform. The capabilities support every stage of development, from generating application components to vibe coding full-stack applications through natural language conversations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/use-ai-capabilities-in-custom-apps.html
release: australia
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 4
keywords: [now assist, app engine, AI capability, AI feature, AI product, AI agent, skill, generative AI, genAI, Now Assist for App Engine, custom app, Now Assist for creator, app generation, code generation, app summarization, UI generation, develop apps]
breadcrumb: [Building applications]
---

# Agentic development on the ServiceNow AI Platform

Build and enhance custom applications using the generative and agentic AI capabilities available on the ServiceNow AI Platform. The capabilities support every stage of development, from generating application components to vibe coding full-stack applications through natural language conversations.

Agentic development on the ServiceNow AI Platform accelerates application development from weeks to minutes, enabling developers of all skill levels to build solutions for their organization's unique workflows. The ServiceNow AI Platform has tools for each stage of application development, from generating flows, to agentically developing entire applications using Build Agent inside ServiceNow Studio or the ServiceNow IDE, and enhancing existing applications with AI skills and agentic workflows.

## Build Agent

Build Agent is an autonomous AI agent that generates full-stack ServiceNow® applications from natural language descriptions. You describe the application you need in the chat panel in ServiceNow Studio or the ServiceNow IDE, and Build Agent generates the necessary code, organizes files, and manages both the core logic and user interface components. You can also ask it general questions about developing on the ServiceNow AI Platform.

Build Agent can enhance existing custom applications with agentic capabilities. It evaluates existing app context, such as tables, roles, business rules, and metadata, and generates in-app agents, skills, and agentic workflows scoped to your application's data model. Generated agents are automatically registered in AI Control Tower for centralized governance, and all artifacts deploy through standard update sets.

For more information, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent.md).

## Agentic development and vibe coding

Agentic development, or vibe coding, is an AI-driven approach to app development in which you build applications through conversations with AI. On the ServiceNow AI Platform, Build Agent makes agentic development possible.

For more information, see [Agentic development on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/vibe-coding-landing.md).

## Now Assist for Creator

Now Assist for Creator includes generative and agentic AI capabilities that can make developing on the ServiceNow AI Platform more efficient. You can use the generative AI skills available with Now Assist for Creator, such as app generation, flow generation, and UI generation. Now Assist for Creator also includes Build Agent, an autonomous AI agent that can develop full-stack applications ready for deployment through conversations using natural language.

For more information, see [Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/now-assist-for-creator-landing.md).

## Now Assist for App Engine

Now Assist for App Engine enables you to enhance custom applications with AI agents and skills that application users can leverage at runtime. With Now Assist for App Engine, you have access to Now Assist AI assets, such as Platform skills, AI agents, and agentic workflows, as well as the tools for developing custom AI assets using Now Assist Skill Kit and AI Agent Studio.

For more information, see [Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md).

## When and where to use AI capabilities

You can use both Now Assist for Creator and Now Assist for App Engine when developing custom applications.

Now Assist for Creator is primarily used when developing, enhancing, or testing custom applications in non-production instances. Creators and developers can use the Now Assist for Creator AI capabilities to quickly build applications and application elements, which are then deployed to production instances.

Now Assist for App Engine is also used when developing custom applications in non-production instances. Creators and developers can modify Now Assist AI assets, or they can create custom skills, AI agents, and agentic workflows. Once the custom application is deployed to a production instance, application users can then leverage the AI assets to help streamline their workflows and improve efficiency.

|Persona|Benefit|Stage in the application life cycle|AI capability|
|-------|-------|-----------------------------------|-------------|
|Developer|Agentically develop entire applications with Build Agent|Development, testing|[Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent.md)|
|Developer|Build and test applications and application elements quickly with generative and agentic AI capabilities.|Development, testing|[Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/now-assist-for-creator-landing.md)|
|Developer|Enhance custom applications with Now Assist AI assets, or build custom skills and agentic workflows.|Development, testing|[Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)|
|Requester, fulfiller, custom application user|Leverage AI assets in custom applications at runtime to help improve productivity and efficiency.|Release, post-release|[Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)|

