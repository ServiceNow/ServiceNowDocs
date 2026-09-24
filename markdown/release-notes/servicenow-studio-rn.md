---
title: ServiceNow Studio release notes
description: The ServiceNow ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps. See the following sections for release notes by version.ServiceNow Studio was enhanced and updated in the September release with an agentic-first, simplified interface for development, and a configurable activity bar.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/servicenow-studio-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Studio release notes

The ServiceNow® ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps. See the following sections for release notes by version.

## About ServiceNow Studio

-   Use the generative and agentic AI capabilities in ServiceNow Studio to build, manage, and deploy custom, base system, or global applications and global metadata records.
-   Access low-code builders available in the ServiceNow AI Platform, including Table Builder and flows in Workflow Studio, alongside other development tools.
-   Package changes for deployment using update sets, pipelines, or the Application Repository without leaving ServiceNow Studio.

See [ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    ServiceNow Studio is a ServiceNow AI Platform feature that is active by default.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/build-automate-rn-landing.md)

## Version 30.1.1

ServiceNow Studio was enhanced and updated in the September release with an agentic-first, simplified interface for development, and a configurable activity bar.

### What's new

-   **[ServiceNow Studio quick start](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-quick-start.md)**

    Learn ServiceNow Studio efficiently with an updated course of quick start topics.

-   **[ServiceNow Studio user interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-user-interface.md)**

    Personalize the new, agentic-first ServiceNow Studio user interface by choosing which components you want to use. Use the pro option with all features, vibe mode with minimal components, or custom, to choose your own.

-   **[Autonomous Engineer in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-autonomous-engineer.md)**

    ServiceNow Studio supports Build Agent spec mode, which generates a complete implementation plan from your requirements.


### What's changed

-   **[ServiceNow Studio settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-settings.md)**

    ServiceNow Studio user preferences and settings have moved from the top right corner to the bottom left corner of the interface. View what's new in ServiceNow Studio, access command palette and keyboard shortcut options, and update preferences.

-   **[App summary generation moves to an agentic architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/sns-exploring-now-assist-app-summarize.md)**

    ServiceNow Otto for app summary generation now uses an AI agent to generate application summaries. This change moves the App summary generation from a skill-based architecture to the AI agent orchestration model.

    With this release, users who install the App summary plugin receive the App Summary AI agent.

    The App Summary AI agent is turned off by default after plugin installation to help avoid unexpected charges. An administrator must enable the agent in AI Agent Studio before users can generate application summaries.

    The end-user experience remains the same. The change affects only the underlying architecture, which now uses an agentic model instead of the earlier skill-based model.

-   **Deployment tab**

    The **Deployment** tab, with lists of all update sets, applications, and deployment requests, has moved from the home page to the activity bar as a separate tab.


### What's deprecated or removed

-   **Experience switcher**

    The Experience switcher has been removed from ServiceNow Studio. ServiceNow IDE capabilities were consolidated under the Explorer tab in ServiceNow Studio. There is no current replacement for the Experience switcher, but each individual application can still be accessed on the ServiceNow AI Platform.

-   **Tools tab**

    The Tools tab has been removed from the ServiceNow Studio home page, with no replacement. For links to documentation for each development tool, see [Integrated development tools for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/integrated-development-tools.md).

-   **Create menu**

    The Create menu in the top right corner of ServiceNow Studio has been removed. The other Create option in the activity bar is still available and has the same functionality.

-   **Resources**

    The Resources section has been removed from the ServiceNow Studio home page. There is no current replacement for the Resources section, but users with Build Agent can prompt in the main chat to access resources.


### Plugin information

-   **Deprecated plugins**

    Studio \(com.glide.dev-studio\): The new ServiceNow Studio \(sn\_sns\) is the replacement for this plugin. For more information, see [Exploring ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-servicenow-studio.md).


