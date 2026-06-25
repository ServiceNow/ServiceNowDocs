---
title: Now Assist for Creator release notes
description: The ServiceNow Now Assist for Creator application includes generative AI skills and AI agents that can help you develop on the ServiceNow AI Platform efficiently. Now Assist for Creator was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-30"
reading_time_minutes: 6
---

# Now Assist for Creator release notes

The ServiceNow® Now Assist for Creator application includes generative AI skills and AI agents that can help you develop on the ServiceNow AI Platform efficiently. Now Assist for Creator was enhanced and updated in the Australia release.

## Now Assist for Creator highlights for the Australia release

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   Upload brand guidelines as a PDF in the theme creation workflow to generate themes that align with your brand.
-   Prepare for the app generation and test generation plugins to be deprecated in a future release.
-   Learn about Build Agent updates in the new [Build Agent release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-agent-rn.md).

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Generate readable documentation throughout the app development life cycle using the new release lifecycle documentation AI agent.
-   Generate themes and color palettes from brand images using the new theme generation workflow in Theme Builder.

Australia early availability

-   Create and update applications in ServiceNow Studio using Build Agent.
-   Generate application modules in UI Builder workspaces using natural-language prompts.
-   Learn how to vibe code using an AI-first approach to development in the new vibe coding documentation.

See  for more information.

**Important:** Now Assist for Creator is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for Creator to Australia

Australia early availability

-   To upgrade the Build Agent application, upgrade the Now Assist for Creator application \(sn\_now\_creator\), which includes the Build Agent Pro plugin \(sn\_build\_agent\_pro\). To upgrade the Build Agent \(Trial\) app, upgrade the sn\_build\_agent plugin.

## New in the Australia release

-   **[Upload brand guidelines to generate theme colors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/tb-create-a-theme-ai.md)**

    Upload brand guidelines as a PDF to the Theme Builder theme creation workflow to generate themes aligned with your brand.


-   ****

    Improve transparency across your app development environment using the release lifecycle documentation AI agent to generate update set descriptions and release notes.

-   **[Generate themes using the new theme generation workflow in Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-theme-now-assist.md)**

    Use the new theme generation workflow in Theme Builder to generate themes based on your brand image. After generating a theme, navigate to Theme Builder to publish and apply additional styling.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   ****

    Use Build Agent in ServiceNow Studio to create and edit full-stack applications conversationally.

-   ****

    Use Now Assist to generate application modules in UI Builder workspaces using natural-language prompts. The Now Assist agent processes your prompts and generates various modules, including lists, records, URLs, scripts, dashboards, and folders.

-   **New vibe coding documentation**

    Read new documentation that introduces vibe coding, which is a natural language approach to application development on the ServiceNow AI Platform. The documentation includes how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


## Changed in this release

-   ****

    Build Agent is the default setting for app generation in ServiceNow Studio. To continue using the app generation skill, change the setting in ServiceNow Studio.


## Removed in this release

Spoke generation has been removed from Now Assist for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

## Activation information

Install Now Assist for Creator by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia Patch 1 release for the release lifecycle documentation AI agent:

    -   App Life Cycle AI Agents \(com.sn\_app\_lc\_agents\): Scoped app: AI agent definition, script includes, REST API, system properties
    -   App Life Cycle AI Agents - Global \(com.glide.app\_lifecycle\_agents.global\): Hosted global plugin: UI actions, UI scripts, global utilities
-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    -   App generation \(sn\_ae\_gen\_ai\): Planned for deprecation in September 2026. The Build Agent plugin provides the latest experience for this functionality.
    -   Test generation \(sn\_text2test\): Planned for deprecation in September 2026. The Build Agent plugin provides the latest experience for this functionality.

## Related ServiceNow applications and features

-   ****

    Track and manage application requests, deployments, and collaborative developers for your custom applications using the App Engine Management Center \(AEMC\).

-   ****

    ServiceNow®Automated Test Framework \(ATF\) enables you to create and run automated tests to confirm that your instance works after making changes.

-   ****

    The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through ac conversational interface.

-   **[Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/catalog-builder.md)**

    ServiceNow® Catalog Builder enables you to create or edit catalog items \(or record producers\) using a visual and guided experience along with specified restrictions. The Catalog Builder experience enables you to delegate the creation and maintenance of the catalog.

-   ****

    The ServiceNow® Creator Studio application is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development.

-   **[Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub.md)**

    Automate integration tasks using ServiceNow® components for Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Use AI recommendations to select the next component in your flow. The system generates recommendations based on the current position in the flow and the flow component names listed before.

-   ****

    ServiceNow® Now Assist for App Engine enables you to enhance custom applications with AI capabilities, such as AI agents and skills, that you can use at runtime.

-   ****

    With the Australia release, the code autocomplete skill of the Now Assist for Code is available in the ServiceNow IDE.

-   **[Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer.md)**

    ServiceNow® Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. You can also use playbooks to provide end users with a simplified, task-oriented view of your process.

-   ****

    ReleaseOps is a solution to problem of deploying changes, customizations, and custom apps on the ServiceNow AI Platform. By automating the deployment process, ReleaseOps helps to increase the predictability and reliability of deployments, while also reducing the risk of releasing unwanted changes to production.

-   **[Robotic Process Automation \(RPA\) Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-bot-generation.md)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.

-   ****

    The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform.

-   **ServiceNow Studio**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps.

-   **[Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-theming.md)**

    The ServiceNow® Theme Builder application enables you to customize the visual experience for your users so that you can update the look and feel to be more like your brand.

-   ****

    The ServiceNow® UI Builder application is a web user interface builder for building pages for workspaces and portals or custom web experiences with Next Experience Components.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio.md)**

    The ServiceNow® Workflow Studio application provides a single location to access all process automation applications.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

