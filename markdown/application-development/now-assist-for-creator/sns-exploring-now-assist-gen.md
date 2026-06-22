---
title: Exploring app generation
description: App generation enables you to create applications in ServiceNow Studio by describing your business process in a conversation with Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/now-assist-for-creator/sns-exploring-now-assist-gen.html
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 4
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [App generation, Use generative AI, Now Assist for Creator, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Exploring app generation

App generation enables you to create applications in ServiceNow Studio by describing your business process in a conversation with Now Assist.

Starting with the Australia release, app generation is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Build Agent provides the latest experience for this functionality. For more information, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent.md).

## How does app generation work?

With the app generation skill available with Now Assist for Creator, you can create applications in ServiceNow Studio using natural language. Describe your business process and engage in a conversation with Now Assist to develop an application for your organization. The application can include a workspace and flows. App generation accelerates the initial development of a basic app that you can then customize.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

Before you begin, confirm that you have the required roles:

-   To use Now Assist, you must have the now\_assist\_panel\_user role.
-   To create an application with the Now Assist for Creator app generation skill, you must have the admin role or the sn\_g\_app\_creator.app\_creator role.
-   To edit \(not create\) an application with app generation, you must have the delegated developer role and be assigned to the application.
-   To add a workspace to an application created using app generation, enable the Now Assist for Creator experience generation skill. For more information, see [Create an AI-generated experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-ui.md).
-   To add a flow to an application created using app generation, enable the Now Assist for Creator flow generation skill and confirm that you have a flow\_designer role. For more information, see [Flow generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/flow-generation-landing.md).

\[Omitted image "app-generation-workflow-infographic-asset-0020323v2.png"\] Alt text: Infographic that shows the four phases to using app generation, with a fifth on verifying the app in ServiceNow Studio.

-   **Conversation**

    Chat with Now Assist to specify the business processes you want in the application. Include details about objectives, users, workflows, and experiences so that Now Assist can generate an accurate initial structure.

-   **Refinement \(generate app requirements and preview\)**

    Now Assist provides a summary of the application requirements based on the conversation. Preview the application to verify that it is accurate. To make changes, continue the conversation and provide additional details. Now Assist updates the preview tab and provides updated summaries until you choose to proceed with generating the application.

-   **App generation**

    Now Assist creates the application and associated components, such as tables, roles, access control lists \(ACLs\), record producers, flows, and workspaces.

-   **Verification**

    In ServiceNow Studio, verify everything that is generated. Modify the app to meet your organization's needs. For example, extend app functionality by adding automation, script includes, business rules, and other features.


On the ServiceNow Studio home page and on the application details tab, apps created with app generation display the AI indicator.

\[Omitted image "app-generation-sns-page-ai-indicator.png"\] Alt text: ServiceNow Studio homepage with an app recently created with app generation highlighted.

## What are the benefits of app generation?

|Benefit|Feature|Users|
|-------|-------|-----|
|Create applications quickly by describing what you need using natural language.|[General guidelines for using app generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-app-gen-guidelines.md)|Developer|
|Refine application details through conversation with Now Assist.|[Generate apps with Now Assist for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-app-gen-using-landing.md)|Developer|
|Edit existing applications faster using Now Assist.|[Review and edit applications built using app generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-app-gen-review-apps.md)|Developer|

-   **[General guidelines for using app generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-app-gen-guidelines.md)**  
To get the best results from app generation, provide clear and detailed descriptions of your application requirements during your conversation with Now Assist.

**Parent Topic:**[App generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-now-assist-app-gen-landing.md)

