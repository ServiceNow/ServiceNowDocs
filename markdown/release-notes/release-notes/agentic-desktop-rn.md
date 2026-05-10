---
title: AI Desktop Actions release notes
description: The ServiceNow AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# AI Desktop Actions release notes

The ServiceNow® AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions was enhanced and updated in the Australia release.

## AI Desktop Actions highlights for the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   The name of the application is now changed to AI Desktop Actions from Agentic Desktop.
-   Use the desktop action to automate dynamic steps that are determined by AI, in addition to automating the recorded steps.
-   Get a quick overview of the AI Desktop Actions application by using the onboarding wizard that highlights steps related to recording, refining, testing, and activating desktop actions.
-   Use the **Show Inputs** / **Show All** buttons in the Test modal to filter required input fields.
-   Use the latest LLM version for improved performance.

[Australia Patch 1](../quality/australia-patch-1.md)

-   Improved error and informational messages for better guidance and troubleshooting.
-   Added a **Delete** button to the image canvas to remove a screen.
-   Enabled screen-level testing while designing desktop actions.

See [AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-landing-page.md) for more information.

## Important information for upgrading AI Desktop Actions to Australia

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

**Important:** AI Desktop Actions is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Use the new application name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-landing-page.md)**

    The product formerly referred to as Agentic Desktop has been rebranded as AI Desktop Actions. All UI labels, navigation elements, and in-product text updated to reflect the new name.

-   **Automate dynamic steps with desktop actions**
    -   Use the desktop action to automate dynamic steps that are determined by AI during execution.
    -   Install the **ServiceNow Web Automation** chrome extension for AI agent to interact with web applications.
    -   Use the default Web Automation Agent AI agent and Web Automation agentic workflow to automate repetitive tasks.
    -   See every click, keystroke, and scroll your AI agent makes in real time, with consent prompts before execution kicks off and timely warnings before your session expires.
    -   Pause a running AI agent, provide corrective input, and resume. The AI agent replans based on your instructions, keeping execution on the right track.
-   **[Use the onboarding wizard to get the app overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/desktop-actions.md)**

    Get a quick overview of the application by using the onboarding wizard that highlights recording, refining, testing, and activating desktop actions.

    Select **Skip intro** to bypass the onboarding wizard and go to the home page. Select the **Don't show this again** option to prevent the wizard from appearing the next time you open the app. After completing the onboarding wizard, select **Get started** to start creating desktop actions.

-   **[Filter required inputs for testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-activate-desktop-action-ad.md)**

    Use filtering options to filter the inputs that are required.

    -   **Show Inputs** — Filters the screens with required input fields.
    -   **Show All** — Removes the filter and displays all screens.

-   **[Improved error and informational messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-activate-desktop-action-ad.md)**

    Improved error and informational messages for better guidance and troubleshooting during testing of desktop actions.

-   **[Delete button on image canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-overview.md)**

    Added a **Delete** button to the image canvas to remove a screen.

-   **[Test button for a screen in the Design tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-overview.md)**

    Test screens directly from the design tab while designing desktop actions.


## UI changes

The system now suggests a full URL instead of a partial URL. For example, `https://<instance name>.servicenow.com`.

Pagination is implemented for desktop actions on the AI Desktop Actions home page, which helps improve navigation and load times.

## Changed in this release

-   **[Optional Application name field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-details-desktop-action-ad.md)**

    The Application field in the Details tab is now optional, enabling you to save and run desktop actions without entering an application name.

-   **[Improved connectors descriptions for non-UI block desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/desktop-actions-designer-workspace-ad.md)**

    Descriptions for Excel, Word, PDF, and System Actions connectors are enhanced to improve accuracy and selection.


## Activation information

AI Desktop Actions is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-agentic-desktop.md).

## Additional requirements

The following are required to use AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md).

You must enable Next Experience UI Framework before you can use the Now Assist panel.

## Browser requirements

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

## Related ServiceNow applications and features

-   **[Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md)**

    The ServiceNow® Now Assist AI agents are entities that mimic human-like intelligence by using large language models \(LLMs\). AI agents can perform tasks that range from simple automated responses to complex problem solving. By using AI agents, you can help reduce the workloads of your live agents and help increase their productivity.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    With the ServiceNow®Now Assist panel, you can get assistance from generative AI experiences to solve customer issues fast. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information quickly.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLMs with your workflows.


**Parent Topic:**[AI Experiences release notes](../analytics-intelligence-reporting/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

