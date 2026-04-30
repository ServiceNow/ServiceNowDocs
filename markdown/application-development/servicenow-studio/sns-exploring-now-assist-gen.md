---
title: Exploring Now Assist for app generation in ServiceNow Studio
description: With Now Assist for app generation, you can create applications through conversations with generative AI.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Now Assist for app generation in ServiceNow Studio, Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Exploring Now Assist for app generation in ServiceNow Studio

With Now Assist for app generation, you can create applications through conversations with generative AI.

## Now Assist for app generation overview

Create applications through a natural conversation with generative AI. Describe your business process and engage in a back-and-forth conversation with Now Assist for app generation to develop an application for your organization. With this feature, your organization can expedite the initial development of a basic app that can then be customized.

In the Yokohama Patch 6 \(August 2025\) release:

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

In the Yokohama Patch 3 \(May 2025\) release:

-   Add a workspace and flows to an application during the conversation with Now Assist for app generation.
-   Both Now LLM Service and Azure OpenAI are supported. For more information, see [Manage large language models](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   To use Now Assist, you must have the now.assist.creator role and the now\_assist\_panel\_user role.
-   To create an application with Now Assist for app generation, you must have the admin role or the sn\_g\_app\_creator.app\_creator role.
-   To edit \(not create\) an application with Now Assist for app generation, you can have the delegated developer role and be assigned to the application.
-   To add a workspace to an application in Now Assist for app generation, the Now Assist Experience Generation skill must be active. For more information, see [Experience generation](../../../administer/ui-generation/task/generate-ui.md).
-   To add a flow to an application in Now Assist for app generation, the Now Assist Flow Generation skill must be active and you must have a flow\_designer role.

![Infographic that shows the four phases to using app generation, with a fifth on verifying the app in ServiceNow Studio.](../images/app-generation-workflow-infographic-asset-0020323v2.png "Now Assist for app generation workflow")

-   **Conversation**

    Chat with Now Assist for app generation to specify the business processes that you want in the application, including the details about the objectives, users, workflows, and experiences.

-   **Refinement \(generate app requirements and preview\)**

    Now Assist for app generation provides a summary of the application requirements based on the information collected during the conversation. Preview the application and check that it’s accurate. If you want to make changes, stay in the conversation and keep editing. Now Assist for app generation continues to update the preview tab based on your comments and provides summaries until you choose to proceed with generating the application.

-   **App generation**

    Now Assist for app generation creates the application and associated components, including the tables, roles, access control lists \(ACLs\), and record producers.

    In the Yokohama Patch 3 \(May 2025\) release, a workspace and flows can be added and generated with the application.

-   **Verification**

    In ServiceNow Studio, verify everything that is generated. Modify the app to make it suit your organization's needs. For example, app functionality can be extended by adding automation, script includes, business rules, and other features.


On the ServiceNow Studio home page and on the application details tab, any apps created with Now Assist for app generation display the AI indicator.

![ServiceNow Studio homepage with an app recently created with Now Assist for app generation highlighted.](../images/app-generation-sns-page-ai-indicator.png)

## App generation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Quickly create applications by describing what you need using natural language.|[General guidelines for using Now Assist for app generation in ServiceNow Studio](sns-app-gen-guidelines.md)|Developer|
|Refine the details of your application through conversation with Now Assist for app generation.|[Generate apps with Now Assist for ServiceNow Studio](../task/sns-app-gen-using-landing.md)|Developer|
|Edit existing applications faster using Now Assist for app generation.|[Review and edit applications using Now Assist for app generation in ServiceNow Studio](../task/sns-app-gen-review-apps.md)|Developer|

-   **[General guidelines for using Now Assist for app generation in ServiceNow Studio](sns-app-gen-guidelines.md)**  
Learn general guidelines for using Now Assist for app generation to create applications with help from generative AI.

**Parent Topic:**[Now Assist for app generation in ServiceNow Studio](sns-now-assist-app-gen-landing.md)

