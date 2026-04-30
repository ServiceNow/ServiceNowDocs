---
title: Use AI capabilities in custom applications
description: Expedite development and enhance custom applications using the generative and agentic AI capabilities available on the ServiceNow AI Platform.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-06-05"
reading_time_minutes: 5
breadcrumb: [Developing your application, Building applications]
---

# Use AI capabilities in custom applications

Expedite development and enhance custom applications using the generative and agentic AI capabilities available on the ServiceNow AI Platform.

When developing custom applications on the ServiceNow AI Platform, you can use different tools to create and enhance your custom applications with AI capabilities, helping to expedite the development process and improve productivity.

## Now Assist for Creator

Now Assist for Creator includes generative AI skills that can make developing on the ServiceNow AI Platform more efficient. Using natural language, you can describe what you want to create, such as a new application using the app generation skill in ServiceNow Studio, or a new form for an application using the form generation skill in Creator Studio. Now Assist for Creator empowers you create, modify, and enhance custom applications and user experiences easily, helping to accelerate development and reduce time-to-value.

The Now Assist for Creator generative AI skills that you can use when building custom applications are listed in the following table.

|Skill|Description|
|-----|-----------|
|[App generation](../../now-assist-app-gen/concept/sns-now-assist-app-gen-landing.md)|Generate simplified apps with AI-generated tables, experiences, and roles tailored to your text prompts.|
|[App summarization](../../now-assist-app-summarize/concept/sns-now-assist-app-summarize-landing.md)|Summarize what an app does using generative AI.|
|[Code generation](https://www.servicenow.com/docs/access?context=now-assist-code-landing&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|Get help writing scripts quickly with AI-generated code based on text or code prompts.|
|[Form generation](../../creator-studio/concept/creator-studio-text-to-form.md)|Create forms by describing what you want using natural language.|
|[Test generation](../../../administer/test-generation/concept/test-generation-intro.md)|Automate test creation from simple descriptions with AI-powered test generation.|
|[UI generation](../../../administer/ui-generation/concept/ui-generation-landing.md)|Create experiences by describing what you want using natural language.|

For more information about Now Assist for Creator, see [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Now Assist for App Engine

Now Assist for App Engine enables you to enhance custom applications with AI agents and skills that application users can leverage at runtime. You can use the Now Assist AI agents and skills that are available with an App Engine Enterprise Plus license. Or you can build custom AI agents and skills using Now Assist Skill Kit and AI Agent Studio that are customized for your application's unique workflow.

For example, let's say that you built a custom application for a sporting goods retail company in ServiceNow Studio. The app enables store employees to manage in-store product inventory and report issues, such as defective merchandise. When an issue is reported, the app automatically notifies the appropriate teams that are responsible for resolution, including product quality assurance, supply chain, and vendor relations. With Now Assist for App Engine, you could create an AI agent in AI Agent Studio that handles some of the time-consuming tasks that fulfiller users of the app would otherwise have to do manually. The AI agent could check whether similar issues have been reported with the product at other store locations, identify recurring product defects, and suggest next steps based on past resolutions. It could even draft a summary of the issue for vendor outreach or escalate urgent cases to the appropriate team, helping to streamline operations and reduce resolution time.

To learn more about the AI capabilities available with Now Assist for App Engine, see [Now Assist for App Engine](../../app-engine-studio/concept/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md).

## When and where to use AI capabilities

You can use both Now Assist for Creator and Now Assist for App Engine when developing custom applications. How and where you implement AI capabilities depends on your organization's workflow and the custom applications that you’re developing.

Now Assist for Creator is primarily used when developing, enhancing, or testing custom applications in non-production instances. Creators and developers can use the Now Assist for Creator skills to quickly build applications and application elements, which are then deployed to production instances.

The AI capabilities available with Now Assist for App Engine are also used when developing custom applications in non-production instances. Creators and developers can use the generative and agentic AI capabilities available with their App Engine Enterprise Plus license to enhance their applications with Now Assist AI agents and skills. Or they can create custom skills and agents that are unique to their app's workflow. Once the applications are deployed to production instances, application users can then leverage the agents and skills to help streamline their workflows and improve efficiency.

|Persona|Benefit|Stage in the application life cycle|AI capability|
|-------|-------|-----------------------------------|-------------|
|Developer|Build and test applications and application elements quickly with generative AI skills.|Development, testing|[Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)|
|Developer|Enhance custom applications with base system AI agents and skills, or build custom AI agents and skills.|Development, testing|[Now Assist for App Engine](../../app-engine-studio/concept/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)|
|Requester, fulfiller, custom application user|Leverage AI agents and skills in custom applications at runtime to help improve productivity and efficiency.|Release, post-release|[Now Assist for App Engine](../../app-engine-studio/concept/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)|

