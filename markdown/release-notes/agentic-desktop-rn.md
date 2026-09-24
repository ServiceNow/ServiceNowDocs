---
title: AI Desktop Actions release notes
description: The ServiceNow AI Desktop Actions application enables you to automate repetitive tasks on your desktop and web. These desktop actions are executed by AI agents created in AI Agent Studio.Adaptive path AI Desktop Actions now gather stored credentials and dynamic parameters automatically, attach and track files during a task, and start faster with fewer stray browser tabs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/agentic-desktop-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [AI Experiences release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# AI Desktop Actions release notes

The ServiceNow® AI Desktop Actions application enables you to automate repetitive tasks on your desktop and web. These desktop actions are executed by AI agents created in AI Agent Studio.

## About AI Desktop Actions

-   Automate multi-step desktop and web tasks that involve conditional logic, freeing your users to focus on work that needs a human touch.
-   Adapt to changes in application state and UI in real-time, reducing the need to maintain rigid scripts.
-   Detect errors during execution and recover by evaluating context and trying alternative approaches.
-   Let AI agents process instructions and generate execution plans autonomously or semi-autonomously, reducing manual setup for repetitive tasks.

See [AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/agentic-desktop-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    AI Desktop Actions is available with activation of any ServiceNow Otto plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-agentic-desktop.md).

-   **Upgrade information**

    Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download AI Desktop Actions installer for defined desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

-   **Browser requirements**

    ServiceNow Otto AI agents support various browsers, including Google Chrome and Microsoft Edge. ServiceNow Otto AI agents aren't supported in Internet Explorer.

-   **Additional requirements**

    The following are required to use defined AI Desktop Actions:

    -   Operating system: Microsoft Windows 11.
    -   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
    -   No extended monitors are connected.
    To use adaptive desktop actions, Web Automation Chrome browser extension is required for web and AI Desktop Actions for macOS is required for desktop and web.

    You must first install the supported ServiceNow Otto version of ServiceNow to be able to use the ServiceNow Otto AI agents. For more information, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-ai-agents-plugins.md).

    You must enable Next Experience UI Framework before you can use the ServiceNow Otto panel.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/intelligent-experiences-rn-landing.md)

## Brazil Patch 0

Adaptive path AI Desktop Actions now gather stored credentials and dynamic parameters automatically, attach and track files during a task, and start faster with fewer stray browser tabs.

### What's new

-   **[Execute adaptive desktop actions on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai_desktop_actions_adaptive.md)**

    Download the new AI Desktop Actions installer for macOS with M-series processor support \(ARM64 architecture\). The adaptive desktop actions enable AI agents to navigate applications and browsers and perform tasks on macOS systems. Both adaptive and defined desktop actions are now available with platform-specific installers.

    -   Review the AI agent's execution plan before it runs and pause execution to make manual adjustments at any time.
    -   Explicit user consent is required before the AI agent can access desktop, third-party services, and files.
    -   Monitor the live execution of adaptive desktop actions in the preview window.
    -   Refer the real-time status tracking that shows whether the AI agent is initiating, running, or paused.
    -   Take control of the execution where your input is needed.
    -   The AI agent batches consecutive actions into single execution calls where possible, minimizing round trips and reducing overall execution time.
-   **[Control resource access using policy and rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/security_policy_governance_concept.md)**

    Create policies and rules to control which resources AI agents can access.

    -   Policies: Collection of resource access rules that applies to a specific user group or set of users based on defined user criteria.
    -   Resource access rules: Specific restrictions controlling agent access to various resource types, such as files, folders, websites, and applications.
    -   Bi-directional policy-rule mapping: Link policies to rules from either the policy record or the rule record, enabling rule reuse across multiple policies.
-   **[Credential and dynamic parameter management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/credential-storage.md)**

    Reference credentials or other user-specific values by name in your instructions. The agent resolves them securely at execution time, so you never have to type them in yourself.

-   **[File upload and download](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/upload-download-file.md)**

    Upload files to web forms and track file downloads during automated browser tasks. The agent validates file safety, confirms the target field with the reasoning model, and escalates to the user when it can't proceed safely.


### What's changed

-   **[Browser startup and tab behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-ai-wa-access-using-nap.md)**

    Browser session now opens to an empty page instead of Google's homepage. Automation actions within the same chat window now reuse the existing browser tab instead of opening a new tab for every action. A new tab opens only when a new chat session starts or you close the current tab.

-   **[Improved security for adaptive desktop actions system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/components-installed-with-agentic-desktop.md)**

    Adaptive desktop actions system properties now require appropriate read and write roles. This change prevents unauthorized users from viewing or modifying the configuration settings, while automation continues to work as expected.


