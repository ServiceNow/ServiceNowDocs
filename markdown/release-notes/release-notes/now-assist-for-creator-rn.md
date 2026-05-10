---
title: Now Assist for Creator release notes
description: The ServiceNow Now Assist for Creator application includes generative AI skills and AI agents that can help you develop on the ServiceNow AI Platform efficiently. Now Assist for Creator was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-30"
reading_time_minutes: 7
---

# Now Assist for Creator release notes

The ServiceNow® Now Assist for Creator application includes generative AI skills and AI agents that can help you develop on the ServiceNow AI Platform efficiently. Now Assist for Creator was enhanced and updated in the Australia release.

## Now Assist for Creator highlights for the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   Upload brand guidelines as a PDF using the theme creation workflow to generate themes that align with your brand.
-   The app generation and test generation plugins are being planned for deprecation in a future release.
-   Learn about Build Agent updates in the new [Build Agent release notes](build-agent-rn.md).

[Australia Patch 1](../quality/australia-patch-1.md)

-   Generate readable documentation throughout the app development lifecycle using the new release lifecycle documentation AI agent.
-   Generate themes and color palettes from brand images using the new theme generation workflow in Theme Builder.

Australia early availability \(March\)

-   Create and update applications in ServiceNow Studio using Build Agent.
-   Generate application modules in UI Builder workspaces using natural-language prompts.
-   Learn how to vibe code, using an AI-first approach to development, in the new vibe coding documentation.

See [Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/now-assist-for-creator-landing.md) for more information.

**Important:** Now Assist for Creator is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for Creator to Australia

Australia early availability \(March\)

-   To upgrade the Build Agent application, upgrade the Now Assist for Creator application \(sn\_now\_creator\), which includes the Build Agent Pro plugin \(sn\_build\_agent\_pro\). To upgrade the Build Agent \(Trial\) app, upgrade the sn\_build\_agent plugin.

## New in the Australia release

-   **[Upload brand guidelines to generate theme colors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/tb-create-a-theme-ai.md)**

    Upload brand guidelines as a PDF to the Theme Builder theme creation workflow to generate themes aligned with your brand.


-   **[Release lifecycle documentation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/release-lifecycle-documentation-agent-landing.md)**

    Improve transparency across your app development environment using the release lifecycle documentation AI agent to generate update set descriptions and release notes seamlessly.

-   **[Generate themes using the new theme generation workflow in Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-theme-now-assist.md)**

    Leverage the new theme generation workflow in Theme Builder to generate themes based on your brand image. After generating a theme, navigate to Theme Builder to publish and apply additional styling.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Build Agent in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/build-agent-in-servicenow-studio.md)**

    Use Build Agent in ServiceNow Studio to create and edit full-stack applications conversationally.

-   **[Generate modules using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-ai-modules.md)**

    Now Assist generates application modules in UI Builder workspaces using natural-language prompts. The Now Assist agent processes your prompts and generates various modules, including lists, records, URLs, scripts, dashboards, and folders.

-   **[New vibe coding documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/vibe-coding-landing.md)**

    Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


## Changed in this release

-   **[Use the app generation skill to generate apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-app-gen-use-app-gen-skill.md)**

    Build Agent is the default setting for app generation in ServiceNow Studio. To continue using the app generation skill, change the setting in ServiceNow Studio.


## Removed in this release

Spoke generation has been removed from Now Assist for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

## Activation information

Install Now Assist for Creator by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

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

-   **[App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/app-engine-management-center.md)**

    Track and manage application requests, deployments, and collaborative developers for your custom applications using the App Engine Management Center \(AEMC\).

-   **[Automated Test Framework \(ATF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-landing-page.md)**

    ServiceNow®Automated Test Framework \(ATF\) enables you to create and run automated tests to confirm that your instance works after making changes.

-   **[Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent.md)**

    The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through ac conversational interface.

-   **[Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-builder.md)**

    ServiceNow® Catalog Builder enables you to create or edit catalog items \(or record producers\) using a visual and guided experience along with specified restrictions. The Catalog Builder experience enables you to delegate the creation and maintenance of the catalog.

-   **[Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-landing.md)**

    The ServiceNow® Creator Studio application is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development.

-   **[Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/integrationhub.md)**

    Automate integration tasks using ServiceNow® components for Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Use AI recommendations to select the next component in your flow. The system generates recommendations based on the current position in the flow and the flow component names listed before.

-   **[Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)**

    ServiceNow® Now Assist for App Engine enables you to enhance custom applications with AI capabilities, such as AI agents and skills, that you can leverage at runtime.

-   **[Now Assist for Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/now-assist-code-landing.md)**

    With the Australia release, the code autocomplete skill of the Now Assist for Code is available in the ServiceNow IDE.

-   **[Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer.md)**

    ServiceNow® Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. You can also use playbooks to provide end users with a simplified, task-oriented view of your process.

-   **[ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/releaseops-landing.md)**

    ReleaseOps is a solution to problem of deploying changes, customizations, and custom apps on the ServiceNow AI Platform. By automating the deployment process, ReleaseOps helps to increase the predictability and reliability of deployments, while also reducing the risk of releasing unwanted changes to production.

-   **[Robotic Process Automation \(RPA\) Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-bot-generation.md)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.

-   **[ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-landing.md)**

    The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform.

-   **[ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-landing.md)**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps.

-   **[Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-theming.md)**

    The ServiceNow® Theme Builder application enables you to customize the visual experience for your users so that you can update the look and feel to be more like your brand.

-   **[UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md)**

    The ServiceNow® UI Builder application is a web user interface builder for building pages for workspaces and portals or custom web experiences with Next Experience Components.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/workflow-studio.md)**

    The ServiceNow® Workflow Studio application provides a single location to access all process automation applications.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

