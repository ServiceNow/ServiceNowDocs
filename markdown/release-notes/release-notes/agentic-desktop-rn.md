---
title: AI Desktop Actions release notes
description: The ServiceNow AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# AI Desktop Actions release notes

The ServiceNow® AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions was enhanced and updated in the Australia release.

## AI Desktop Actions highlights for the Australia release

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Record desktop actions more accurately by using the new AI-powered recording mode when creating desktop actions.
-   Save time on manual setup by letting AI automatically insert anchors and generate screen context for each captured screen and add desktop action description after recording.
-   Switch between AI-assisted recording and manual recording by using the new **Record with AI \(recommended\)** check box that replaces the previous capture modes in the Create Desktop Action dialog.
-   Make desktop actions more flexible by configuring parameters for on-screen task desktop actions.
-   Pass dynamic values at runtime by mapping parameters in the Map parameters section in AI Agent Studio.
-   Control data visibility and security by using the **Shared** and **Mark As Sensitive** fields on the Desktop action parameter form.
-   Get a quick guidance on how to effectively use the recorder with the recorder tips modal.
-   Keep browser tabs open after an adaptive desktop action completes by using the **sn\_naa.keep\_tab\_open** system property. The property is enabled by default.
-   Use the enhanced adaptive desktop actions to improve execution efficiency.

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   The name of the application is now changed to AI Desktop Actions from Agentic Desktop.
-   Use the desktop action to automate dynamic steps that are determined by AI, and automating the recorded steps.
-   Get a quick overview of the AI Desktop Actions application by using the onboarding wizard that highlights steps related to recording, refining, testing, and activating desktop actions.
-   Use the **Show Inputs** / **Show All** buttons in the Test modal to filter required input fields.
-   Use the latest LLM version for improved performance.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Improved error and informational messages for better guidance and troubleshooting.
-   Added a **Delete** button to the image canvas to remove a screen.
-   Enabled screen-level testing while designing desktop actions.

See [AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-landing-page.md) for more information.

## Important information for upgrading AI Desktop Actions to Australia

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

## New in the Australia release

-   **[Record desktop actions with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/record-with-ai-ad.md)**

    -   Record on-screen task desktop actions using AI to automatically validate anchor positions and generate screen contexts at design time, reducing automation failures caused by fragile anchors at testing or runtime.
    -   Use a new role, sn\_desktop\_core.desktop\_action\_user that enables users to record desktop action with AI.
    -   Enable AI to analyze the recording in three stages: analyzing the recording, inserting anchors, and generating screen contexts by selecting **Record with AI \(recommended\)** in the **Create desktop action** dialog and finish recording.
    -   Identify AI-generated anchors and screen contexts that are marked with an AI badge in the properties panel. Each screen includes an editable screen context that helps AI agents understand the screen's intent at runtime.
    -   Regenerate screen context and anchor positions that don't meet your expectations by selecting **Retry** in the screen properties panel.
    -   Resolve anchor issues before activation by responding to the alert that appears when any screens have failed anchors in a desktop action recorded with AI.
    -   Reduce manual setup time by letting AI auto-fill the desktop action intent in the **Action description** field when you select the **Record with AI** option. An AI badge confirms that the description was filled by AI.
    -   Control whether **Record with AI** is the default recording option by configuring the new **sn\_desktop\_core.record\_with\_ai** property. By default, its value is set to true.
    **Important:** Record with AI requires the ServiceNow AI Lens skill to be active and you must have the sn\_desktop\_core.desktop\_action\_user role. If any of these conditions is not met, the **Record with AI** option is unavailable. You can still create desktop actions using auto-capture mode. Contact your ServiceNow administrator to enable these settings.

-   **[Configure parameters for dynamic values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-parameter-record-ad.md)**

    -   Provide dynamic values, such as credentials and user-specific inputs to on-screen task desktop actions by creating Desktop action parameter records in your ServiceNow instance.
    -   Make a single stored parameter value available to all users by selecting the **Shared** field on a parameter record. When **Shared** is selected, the agent uses the one associated parameter value record, regardless of which user triggered the agent. Only a user with the sn\_aia.admin role can create the parameter value record for a shared parameter.
    -   Encrypt all associated parameter value records by selecting the **Mark As Sensitive** field on a parameter record. The agent decrypts the value at execution time. For non-sensitive parameters, the value is passed to the agent as plain text.
    -   In the AI Desktop Actions client application, enable the Set Text and Send Keys step types to use parameters by selecting the **Use parameter** property.
    -   In AI Agent Studio, when you add an on-screen task desktop action tool that contains inputs configured for parameters, the **Map parameters** section appears. You can map inputs of on-screen task desktop actions to parameter records. These parameter values aren't exposed in agent instructions. Select a parameter record for each input to define the value the AI agent uses when executing the desktop action.
    **Important:**

    The **Shared** and **Mark As Sensitive** fields can only be modified when no Desktop action parameter value records exist under the parameter record.


-   **[Use the new application name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-landing-page.md)**

    The product formerly referred to as Agentic Desktop has been rebranded as AI Desktop Actions. All UI labels, navigation elements, and in-product text updated to reflect the new name.

-   **[Automate dynamic steps with desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/web-agents-overview.md)**
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

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLMs with your workflows.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

