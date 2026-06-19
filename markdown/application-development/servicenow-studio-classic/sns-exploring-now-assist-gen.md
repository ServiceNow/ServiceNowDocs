---
title: Exploring Now Assist for app generation in ServiceNow Studio
description: With Now Assist for app generation, you can create applications through conversations with generative AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-exploring-now-assist-gen.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Now Assist for app generation in ServiceNow Studio, Now Assist tools and AI files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Exploring Now Assist for app generation in ServiceNow Studio

With Now Assist for app generation, you can create applications through conversations with generative AI.

## Now Assist for app generation overview

Create applications through a natural conversation with generative AI. Describe your business process and engage in a back-and-forth conversation with Now Assist for app generation to develop an application for your organization. The application can include a workspace and flows. With this feature, your organization can expedite the initial development of a basic app that can then be customized.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see .

-   To use Now Assist, you must have the now\_assist\_panel\_user role.
-   To create an application with Now Assist for app generation, you must have the admin role or the sn\_g\_app\_creator.app\_creator role.
-   To edit \(not create\) an application with Now Assist for app generation, you can have the delegated developer role and be assigned to the application.
-   To add a workspace to an application in Now Assist for app generation, the Now Assist Experience Generation skill must be active. For more information, see [Experience generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/generate-ui.md).
-   To add a flow to an application in Now Assist for app generation, the Now Assist Flow Generation skill must be active and you must have a flow\_designer role. For more information, see .

\[Omitted image "app-generation-workflow-infographic-asset-0020323v2.png"\] Alt text: Infographic that shows the four phases to using app generation, with a fifth on verifying the app in ServiceNow Studio.

-   **Conversation**

    Chat with Now Assist for app generation to specify the business processes that you want in the application, including the details about the objectives, users, workflows, and experiences.

-   **Refinement \(generate app requirements and preview\)**

    Now Assist for app generation provides a summary of the application requirements based on the information collected during the conversation. Preview the application and check that it’s accurate. If you want to make changes, stay in the conversation and keep editing. Now Assist for app generation continues to update the preview tab based on your comments and provides summaries until you choose to proceed with generating the application.

-   **App generation**

    Now Assist for app generation creates the application and associated components, such as tables, roles, access control lists \(ACLs\), record producers, flows, and a workspace.

-   **Verification**

    In ServiceNow Studio, verify everything that is generated. Modify the app to make it suit your organization's needs. For example, app functionality can be extended by adding automation, script includes, business rules, and other features.


On the ServiceNow Studio home page and on the application details tab, any apps created with Now Assist for app generation display the AI indicator.

\[Omitted image "app-generation-sns-page-ai-indicator.png"\] Alt text: ServiceNow Studio homepage with an app recently created with Now Assist for app generation highlighted.

## App generation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Quickly create applications by describing what you need using natural language.|[General guidelines for using Now Assist for app generation in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-app-gen-guidelines.md)|Developer|
|Refine the details of your application through conversation with Now Assist for app generation.|[Generate apps with Now Assist for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-app-gen-using-landing.md)|Developer|
|Edit existing applications faster using Now Assist for app generation.|[Review and edit applications using Now Assist for app generation in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-app-gen-review-apps.md)|Developer|

-   **[General guidelines for using Now Assist for app generation in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-app-gen-guidelines.md)**  
Learn general guidelines for using Now Assist for app generation to create applications with help from generative AI.

**Parent Topic:**[Now Assist for app generation in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-now-assist-app-gen-landing.md)

