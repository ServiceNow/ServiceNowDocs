---
title: Exploring app generation
description: App generation enables you to create applications in ServiceNow Studio by describing your business process in a conversation with Now Assist.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [App generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Exploring app generation

App generation enables you to create applications in ServiceNow Studio by describing your business process in a conversation with Now Assist.

## How does app generation work?

With the app generation skill available with Now Assist for Creator, you can create applications in ServiceNow Studio using natural language. Describe your business process and engage in a conversation with Now Assist to develop an application for your organization. The application can include a workspace and flows. App generation accelerates the initial development of a basic app that you can then customize.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Before you begin, confirm that you have the required roles:

-   To use Now Assist, you must have the now\_assist\_panel\_user role.
-   To create an application with the Now Assist for Creator app generation skill, you must have the admin role or the sn\_g\_app\_creator.app\_creator role.
-   To edit \(not create\) an application with app generation, you must have the delegated developer role and be assigned to the application.
-   To add a workspace to an application created using app generation, enable the Now Assist for Creator experience generation skill. For more information, see [Experience generation](../../../administer/ui-generation/task/generate-ui.md).
-   To add a flow to an application created using app generation, enable the Now Assist for Creator flow generation skill and confirm that you have a flow\_designer role. For more information, see [Flow generation](../../../administer/flow-designer/reference/flow-generation-landing.md).

![Infographic that shows the four phases to using app generation, with a fifth on verifying the app in ServiceNow Studio.](../images/app-generation-workflow-infographic-asset-0020323v2.png "App generation workflow")

-   **Conversation**

    Chat with Now Assist to specify the business processes you want in the application. Include details about objectives, users, workflows, and experiences so that Now Assist can generate an accurate initial structure.

-   **Refinement \(generate app requirements and preview\)**

    Now Assist provides a summary of the application requirements based on the conversation. Preview the application to verify that it is accurate. To make changes, continue the conversation and provide additional details. Now Assist updates the preview tab and provides updated summaries until you choose to proceed with generating the application.

-   **App generation**

    Now Assist creates the application and associated components, such as tables, roles, access control lists \(ACLs\), record producers, flows, and workspaces.

-   **Verification**

    In ServiceNow Studio, verify everything that is generated. Modify the app to meet your organization's needs. For example, extend app functionality by adding automation, script includes, business rules, and other features.


On the ServiceNow Studio home page and on the application details tab, apps created with app generation display the AI indicator.

![ServiceNow Studio homepage with an app recently created with app generation highlighted.](../images/app-generation-sns-page-ai-indicator.png)

## What are the benefits of app generation?

|Benefit|Feature|Users|
|-------|-------|-----|
|Create applications quickly by describing what you need using natural language.|[General guidelines for using app generation](sns-app-gen-guidelines.md)|Developer|
|Refine application details through conversation with Now Assist.|[Generate apps with Now Assist for ServiceNow Studio](../task/sns-app-gen-using-landing.md)|Developer|
|Edit existing applications faster using Now Assist.|[Review and edit applications built using app generation](../task/sns-app-gen-review-apps.md)|Developer|

-   **[General guidelines for using app generation](sns-app-gen-guidelines.md)**  
To get the best results from app generation, provide clear and detailed descriptions of your application requirements during your conversation with Now Assist.

**Parent Topic:**[App generation](sns-now-assist-app-gen-landing.md)

