---
title: ServiceNow Otto for Creator release notes
description: The ServiceNow ServiceNow Otto for Creator application includes generative AI skills that can help you develop on the ServiceNow AI Platform efficiently. ServiceNow Otto for Creator was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-30"
reading_time_minutes: 12
keywords: [Now Assist, Now Assist for Creator, AI features, AI products, solutions, Gen AI, Build Agent]
---

# ServiceNow Otto for Creator release notes

The ServiceNow® ServiceNow Otto for Creator application includes generative AI skills that can help you develop on the ServiceNow AI Platform efficiently. ServiceNow Otto for Creator was enhanced and updated in the Zurich release.

## ServiceNow Otto for Creator highlights for the Zurich release

[Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)

-   Upload brand guidelines as a PDF to the Theme Builder theme creation workflow to generate themes aligned with your brand.
-   Leverage the new widget generation and widget updation skills to create widgets and modify existing widgets within the Next Experience UI Framework using natural language prompts.
-   Troubleshoot Automated Test Framework \(ATF\) tests using the Test Agent available in the Build Agent chat panel.
-   Use the Build Agent semantic search tool to find files, applications, and knowledge on your instance.
-   Validate your UI output in real-time using the Build Agent UI validation tool.
-   Use Build Agent to create agentic workflows, agents, and skills.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Build Agent is now available in ServiceNow Studio.
-   Leverage improved large language model \(LLM\) support with Build Agent.
-   With Build Agent, you can edit entire instances, not just individual apps.
-   Build Agent features extended metadata support, such as flows, Service Catalog workspaces, UI components, list controls, UI policies, and emails.
-   A new granular admin role enables users to use the mobile card generation skill.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Generate themes and color palettes from brand images using the new theme generation workflow in Theme Builder.
-   Edit published or live catalog items directly through conversations with Now Assist.
-   Configure UI policies, location, access, fulfillment, and portal settings for catalog items with the catalog item generation skill.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.
-   Expedite the troubleshooting process by using the ATF troubleshooting agent store application.
-   Learn about how to use UI Builder and modify UI pages with the UI Builder agent.
-   Plan your application development with the Build Agent planning tool.
-   Generate catalog items conversationally and preview them during the creation process with Now Assist in Catalog Builder.

[Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)

-   Accelerate the transition from application design to development by connecting the Build Agent to the Figma Model Context Protocol server.

[Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)

-   Try the Build Agent for free with the Build Agent \(Trial\).

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Create, edit, and deploy fully functional ServiceNow applications using the Build Agent in the ServiceNow IDE.
-   Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities.

See [ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/now-assist-for-creator-landing.md) for more information.

**Important:** ServiceNow Otto for Creator is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Upload brand guidelines to generate theme colors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/tb-create-a-theme-ai.md)**

    Upload brand guidelines as a PDF to the Theme Builder theme creation workflow to generate themes aligned with your brand.

-   **[Test Agent for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/build-agent-testing.md)**

    The Test Agent can now execute Automated Test Framework \(ATF\) tests right from the Build Agent chat panel for test artifacts created in the same session. When tests fail, the tests and test results generated by Test Agent after execution are saved in the standard ATF record tables and can be scheduled for continued regression testing for the app. If tests were edited by the test agent after troubleshooting, those edits are automatically saved to the test records.

-   **[Semantic search for instance artifact discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/build-agent-tools.md)**

    Use semantic search in Build Agent to locate relevant instance artifacts, including tables, scripts, and business rules during build and edit tasks. Find files, applications, and knowledge on your instance based on meaning instead of requiring exact keywords.

-   **[UI validation tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

    Validate user interface output automatically during Build Agent app creation using the integrated UI validation, which runs Playwright-based UI checks on Cloud Runner and surfaces failures with diagnostic context directly in the Build Agent panel.

-   **[Create agentic workflows, agents, and skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/create-custom-ai-agent.md)**

    Turn business requirements into fully configured agents, skills, and agentic workflows for your custom applications. Build Agent inspects your app's existing tables, roles, business rules, and metadata to create tailored in-app agents, complete with the tools needed to support your specific use case.


-   **[Build Agent in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/build-agent-in-servicenow-studio.md)**

    Access Build Agent in ServiceNow Studio to build apps conversationally in a consolidated development environment.

-   **[Improved LLM support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

    Support for Opus 4.6 and Sonnet 4.5 is now available in Build Agent to provide better contextual conversations.

-   **[New metadata support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/build-agent-supported-metadata.md)**

    Work with more metadata types, as Build Agent now supports working with the following:

    -   Email integration
    -   List controls
    -   Service Catalog items
    -   UI components
    -   UI policies
    -   UI views
    -   Workspaces

-   **[Generate themes using the new theme generation workflow in Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/create-theme-now-assist.md)**

    Leverage the new theme generation workflow in Theme Builder to generate themes based on your brand image. After generating a theme, navigate to Theme Builder to publish and apply additional styling.

-   **[Edit already published catalog items using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/edit-already-published-catalog-items-using-now-assist.md)**

    Edit and refine published catalog items conversationally using Now Assist in Catalog Builder.

-   **[Generate UI policies in Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-ui-policy-functions.md)**

    Use Now Assist to create new UI policies, update existing ones, and deactivate them, all through simple, conversational prompts. Each UI policy can include multiple actions, and Now Assist can create that for you.

-   **[Assign catalog item location with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/setting-location-catalog-category-and-topic-with-now-assist.md)**

    When creating or editing a catalog item, you can use plain language to assign values for catalog, category, or topic. If the value you provide matches an existing entry, Now Assist automatically applies it to the item, helping to streamline the process and reduce manual data entry.


-   **[Configure AI model providers for ServiceNow Otto for Code skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/scripts/configure-model-providers-for-now-assist-skills.md)**

    Choose a model provider for ServiceNow Otto for Code skills in the script editor. You can choose from the models that are enabled in the AI Control Tower.

-   **[Planning tool available with the Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

    Build a detailed, step-by-step plan for your application development with the Build Agent planning tool. You can refine the plan iteratively by prompting for changes and providing feedback until you reach a final version.

-   **[Build Agent supports Azure OpenAI and Google Gemini](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/install-build-agent.md)**

    Use Build Agent with Azure OpenAI and Google Gemini in addition to Anthropic Claude on AWS.

-   **[Use images as prompts in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

    Attach images, such as architectural diagrams or UI wireframes, to provide context for prompts in the Build Agent.

-   **[Generate catalog items conversationally with Now Assist in Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/create-catalog-item-using-now-assist.md)**

    Create catalog items and record producers efficiently using the conversational interface within Catalog Builder. Communicate your requirements and specifications for your desired catalog items through guided conversation. Now Assist for catalog generation helps to simplify and streamline the catalog item creation process.

-   **[Preview catalog items during the creation process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/create-catalog-item-using-now-assist.md)**

    Preview catalog items during the creation process. Quick previews enable you to verify that catalog items appear and function as intended before publication.

-   **[Getting help with the Now Assist panel in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/uib-now-assist-panel.md)**

    Create pages using natural language text prompts with Now Assist in UI Builder. Quickly add layouts, components, and content to your pages without manually configuring each element. You can also quickly analyze page structure and data flow by asking questions using natural language.

-   **[Key features of UI Builder agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/key-features-of-ui-builder-agent.md)**

    Ask your questions about using UI Builder to the UI Builder agent. The UI Builder agent provides an overview of page configuration, such as the structure and interconnections of page elements. You can also use the UI Builder agent to apply different layouts, configure components, and update styling.

-   **[ATF troubleshooting agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/atf-troubleshooting-agent-landing-page.md)**

    Accelerate troubleshooting and resolve test failures quickly by using ATF troubleshooting agent on covered metadata.


-   **[MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/accelerate-design-to-development-with-figma-mcp-server.md)**

    You can now connect the Build Agent to the Figma MCP server. The Figma MCP server enables the Build Agent to access the structured data within Figma files. This connection accelerates the transition from application design to development, helping to make the developer workflow more efficient.


-   **[New Build Agent \(Trial\) available](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

    A trial version of the Build Agent is now available with Build Agent \(Trial\). With Build Agent \(Trial\), you can explore limited interactions with the Build Agent for free.


-   **[New third-party AI model provider options available for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md)**

    Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.

-   **[Build Agent, an autonomous AI agent for ServiceNow application development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

    The Build Agent, located in a chat panel within the ServiceNow IDE, functions as an autonomous AI agent capable of independently generating a complete ServiceNow application. It can handle various code-related tasks, such as rewriting tables, explaining code, validating and improving existing applications, fixing application errors, and more.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Removed in this release

[Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)

-   Spoke generation has been removed from ServiceNow Otto for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Starting with version 28.4.3 of ServiceNow Otto for Creator, the now.assist.creator role has been removed as a required role for using most ServiceNow Otto for Creator skills and agents. Some skills and agents might have additional role requirements. See the [ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/now-assist-for-creator-landing.md) product documentation for more information.

## Activation information

Install ServiceNow Otto for Creator by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/creator-studio-landing.md)**

    The ServiceNow® Creator Studio application is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development.

-   **[Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integrationhub.md)**

    Automate integration tasks using ServiceNow® components for Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/spokes-list.md)**

    Activate spokes to enhance your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.

-   **[MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/mid-server-landing.md)**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Use AI recommendations to select the next component in your flow. The system generates recommendations based on the current position in the flow and the flow component names listed before.

-   **[ServiceNow Otto for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)**

    ServiceNow® ServiceNow Otto for App Engine enables you to enhance custom applications with AI capabilities, such as AI agents and skills, that you can leverage at runtime.

-   **[ServiceNow Otto for Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/scripts/now-assist-code-landing.md)**

    With the Zurich release, the code autocomplete skill of the ServiceNow Otto for Code is available in the ServiceNow IDE.

-   **[Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer.md)**

    ServiceNow® Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. You can also use playbooks to provide end users with a simplified, task-oriented view of your process.

-   **[Robotic Process Automation \(RPA\) Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/rpa-main-landing-page.md)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.

-   **[ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-ide-landing.md)**

    The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform.

-   **[ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-studio-landing.md)**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps.

-   **[UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder-overview.md)**

    The ServiceNow® UI Builder application is a web user interface builder for building pages for workspaces and portals or custom web experiences with Next Experience Components.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    The ServiceNow® Workflow Studio application provides a single location to access all process automation applications.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

