---
title: Combined AI Desktop Actions release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for AI Desktop Actions from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-aidesktopactions-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined AI Desktop Actions release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for AI Desktop Actions from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Desktop Actions release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Desktop Actions to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download installer](https://www.servicenow.com/docs/access?context=download-agentic-desktop-installer&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download installer](https://www.servicenow.com/docs/access?context=download-agentic-desktop-installer&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for AI Desktop Actions.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Support for different screen resolutions and scaling](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&family=zurich&ft:locale=en-US)**

Desktop actions now run reliably on machines with different screen resolutions and scaling. Screen resolution and scaling are consistent across all screens of a desktop actions during creation, saving, and publishing.


-   **[Design UI block desktop actions in Design workspace](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&family=zurich&ft:locale=en-US)**

Design, configure, and manage desktop actions in the Design workspace that enables:

    -   Auto-recording or manually capturing screens and defining UI interactions, such as clicking buttons, typing into text boxes, and selecting from drop-down menus.
    -   Adding details such as name, description, input and output parameters.
    -   Testing desktop actions before activating them.
    -   Publishing desktop actions to AI Agent Studio as tools for AI agents to execute.
Example: Filling out fields and submitting a form.

-   **[Use non-UI block desktop actions](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&family=zurich&ft:locale=en-US)**

Add default desktop actions of the type non-UI block as tools to AI agents in AI Agent Studio. The non-UI block actions include pre-built connectors that enable your agentic workflows to interact with various applications and system components. These connectors streamline automation by offering pre-built actions for common tasks, reducing the need for complex scripting.

Each connector focuses on a specific application or system area, providing a collection of related actions. For example, the Microsoft Outlook connector offers actions for email management, while the File and Directory connector provides actions for file system operations.

The following connectors are supported:

    -   Microsoft Excel
    -   Microsoft Outlook
    -   Microsoft Word
    -   PDF
    -   PowerShell
    -   SQL
    -   SSH
    -   SystemAction
Example: Reading data from Microsoft Excel or emails from Microsoft Outlook.

-   **[Adding desktop actions to AI agents in AI Agent Studio](https://www.servicenow.com/docs/access?context=create-ai-agents-ad&family=zurich&ft:locale=en-US)**

Seamless integration with AI Agent Studio has enabled effortless configuration of desktop actions to automate repetitive tasks on applications without APIs. AI agents can reason, plan, and execute desktop actions autonomously and semi-autonomously across legacy systems and desktop applications without complex setups.

-   **[Monitor desktop actions in Execution workspace](https://www.servicenow.com/docs/access?context=use-agentic-desktop&family=zurich&ft:locale=en-US)**

Trigger desktop actions from the Now Assist panel that are executed by AI agents in the Execution workspace. Interact with the automation when human input is required. These automations run in the background and listen for instructions dispatched from the ServiceNow instance. You can continue working on other desktop applications outside Execution workspace.

-   **[Leverage core desktop capabilities](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&family=zurich&ft:locale=en-US)**

Automate form filling, application clicks, and Windows OS file handling. Create workflows across legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.


</td></tr><tr><td>

Australia

</td><td>

-   **[Record desktop actions with AI](https://www.servicenow.com/docs/access?context=record-with-ai-ad&family=australia&ft:locale=en-US)**

    -   Record on-screen task desktop actions using AI to automatically validate anchor positions and generate screen contexts at design time, reducing automation failures caused by fragile anchors at testing or runtime.
    -   Use a new role, sn\_desktop\_core.desktop\_action\_user that enables users to record desktop action with AI.
    -   Enable AI to analyze the recording in three stages: analyzing the recording, inserting anchors, and generating screen contexts by selecting **Record with AI \(recommended\)** in the **Create desktop action** dialog and finish recording.
    -   Identify AI-generated anchors and screen contexts that are marked with an AI badge in the properties panel. Each screen includes an editable screen context that helps AI agents understand the screen's intent at runtime.
    -   Regenerate screen context and anchor positions that don't meet your expectations by selecting **Retry** in the screen properties panel.
    -   Resolve anchor issues before activation by responding to the alert that appears when any screens have failed anchors in a desktop action recorded with AI.
    -   Reduce manual setup time by letting AI auto-fill the desktop action intent in the **Action description** field when you select the **Record with AI** option. An AI badge confirms that the description was filled by AI.
    -   Control whether **Record with AI** is the default recording option by configuring the new **sn\_desktop\_core.record\_with\_ai** property. By default, its value is set to true.
**Important:** Record with AI requires the ServiceNow AI Lens skill to be active and you must have the sn\_desktop\_core.desktop\_action\_user role. If any of these conditions is not met, the **Record with AI** option is unavailable. You can still create desktop actions using auto-capture mode. Contact your ServiceNow administrator to enable these settings.

-   **[Configure parameters for dynamic values](https://www.servicenow.com/docs/access?context=configure-parameter-record-ad&family=australia&ft:locale=en-US)**

    -   Provide dynamic values, such as credentials and user-specific inputs to on-screen task desktop actions by creating Desktop action parameter records in your ServiceNow instance.
    -   Make a single stored parameter value available to all users by selecting the **Shared** field on a parameter record. When **Shared** is selected, the agent uses the one associated parameter value record, regardless of which user triggered the agent. Only a user with the sn\_aia.admin role can create the parameter value record for a shared parameter.
    -   Encrypt all associated parameter value records by selecting the **Mark As Sensitive** field on a parameter record. The agent decrypts the value at execution time. For non-sensitive parameters, the value is passed to the agent as plain text.
    -   In the AI Desktop Actions client application, enable the Set Text and Send Keys step types to use parameters by selecting the **Use parameter** property.
    -   In AI Agent Studio, when you add an on-screen task desktop action tool that contains inputs configured for parameters, the **Map parameters** section appears. You can map inputs of on-screen task desktop actions to parameter records. These parameter values aren't exposed in agent instructions. Select a parameter record for each input to define the value the AI agent uses when executing the desktop action.
**Important:**

The **Shared** and **Mark As Sensitive** fields can only be modified when no Desktop action parameter value records exist under the parameter record.


-   **[Use the new application name](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=australia&ft:locale=en-US)**

The product formerly referred to as Agentic Desktop has been rebranded as AI Desktop Actions. All UI labels, navigation elements, and in-product text updated to reflect the new name.

-   **[Automate dynamic steps with desktop actions](https://www.servicenow.com/docs/access?context=web-agents-overview&family=australia&ft:locale=en-US)**
    -   Use the desktop action to automate dynamic steps that are determined by AI during execution.
    -   Install the **ServiceNow Web Automation** chrome extension for AI agent to interact with web applications.
    -   Use the default Web Automation Agent AI agent and Web Automation agentic workflow to automate repetitive tasks.
    -   See every click, keystroke, and scroll your AI agent makes in real time, with consent prompts before execution kicks off and timely warnings before your session expires.
    -   Pause a running AI agent, provide corrective input, and resume. The AI agent replans based on your instructions, keeping execution on the right track.
-   **[Use the onboarding wizard to get the app overview](https://www.servicenow.com/docs/access?context=desktop-actions&family=australia&ft:locale=en-US)**

Get a quick overview of the application by using the onboarding wizard that highlights recording, refining, testing, and activating desktop actions.

Select **Skip intro** to bypass the onboarding wizard and go to the home page. Select the **Don't show this again** option to prevent the wizard from appearing the next time you open the app. After completing the onboarding wizard, select **Get started** to start creating desktop actions.

-   **[Filter required inputs for testing](https://www.servicenow.com/docs/access?context=test-activate-desktop-action-ad&family=australia&ft:locale=en-US)**

Use filtering options to filter the inputs that are required.

    -   **Show Inputs** — Filters the screens with required input fields.
    -   **Show All** — Removes the filter and displays all screens.

-   **[Improved error and informational messages](https://www.servicenow.com/docs/access?context=test-activate-desktop-action-ad&family=australia&ft:locale=en-US)**

Improved error and informational messages for better guidance and troubleshooting during testing of desktop actions.

-   **[Delete button on image canvas](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&family=australia&ft:locale=en-US)**

Added a **Delete** button to the image canvas to remove a screen.

-   **[Test button for a screen in the Design tab](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&family=australia&ft:locale=en-US)**

Test screens directly from the design tab while designing desktop actions.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing AI Desktop Actions features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Optional Application name field](https://www.servicenow.com/docs/access?context=add-details-desktop-action-ad&family=australia&ft:locale=en-US)**

The Application field in the Details tab is now optional, enabling you to save and run desktop actions without entering an application name.

-   **[Improved connectors descriptions for non-UI block desktop actions](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&family=australia&ft:locale=en-US)**

Descriptions for Excel, Word, PDF, and System Actions connectors are enhanced to improve accuracy and selection.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some AI Desktop Actions features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some AI Desktop Actions features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Desktop Actions.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

AI Desktop Actions is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure](https://www.servicenow.com/docs/access?context=configure-agentic-desktop&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

AI Desktop Actions is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure](https://www.servicenow.com/docs/access?context=configure-agentic-desktop&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Desktop Actions we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The following are required to use AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

 You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).

 You must enable Next Experience UI Framework before you can use the Now Assist panel.

</td></tr><tr><td>

Australia

</td><td>

The following are required to use AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

 You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=australia&ft:locale=en-US).

 You must enable Next Experience UI Framework before you can use the Now Assist panel.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Desktop Actions we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

</td></tr><tr><td>

Australia

</td><td>

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Desktop Actions, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Desktop Actions we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Desktop Actions we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   Record desktop actions more accurately by using the new AI-powered recording mode when creating desktop actions.
-   Save time on manual setup by letting AI automatically insert anchors and generate screen context for each captured screen and add desktop action description after recording.
-   Switch between AI-assisted recording and manual recording by using the new **Record with AI \(recommended\)** check box that replaces the previous capture modes in the Create Desktop Action dialog.
-   Make desktop actions more flexible by configuring parameters for on-screen task desktop actions.
-   Pass dynamic values at runtime by mapping parameters in the Map parameters section in AI Agent Studio.
-   Control data visibility and security by using the **Shared** and **Mark As Sensitive** fields on the Desktop action parameter form.
-   Get a quick guidance on how to effectively use the recorder with the recorder tips modal.
-   Keep browser tabs open after an adaptive desktop action completes by using the **sn\_naa.keep\_tab\_open** system property. The property is enabled by default.
-   Use the enhanced adaptive desktop actions to improve execution efficiency.

 [Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US)

-   The name of the application is now changed to AI Desktop Actions from Agentic Desktop.
-   Use the desktop action to automate dynamic steps that are determined by AI, and automating the recorded steps.
-   Get a quick overview of the AI Desktop Actions application by using the onboarding wizard that highlights steps related to recording, refining, testing, and activating desktop actions.
-   Use the **Show Inputs** / **Show All** buttons in the Test modal to filter required input fields.
-   Use the latest LLM version for improved performance.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Improved error and informational messages for better guidance and troubleshooting.
-   Added a **Delete** button to the image canvas to remove a screen.
-   Enabled screen-level testing while designing desktop actions.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Use smart sizing in the Execution workspace with the **Fit to window** and **Original resolution** options.
-   Enable AI agents to securely access SSH parameters by setting up parameter records in the ServiceNow instance.
-   Test specific screens within desktop actions without running the entire flow.
-   Access application controls during recording with a recorder toolbar.
-   Configure the AI Desktop Actions installer experience for settings that are essential for seamless execution of desktop actions.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Desktop actions now run reliably on machines with different screen resolutions.

 -   Design desktop actions of type UI block \(UI actions\) by capturing user interactions, adding details, and activating them in Design workspace.
-   Use default desktop actions of type non-UI block \(non-UI actions\) that include pre-built connectors to interact with various applications and system components.
-   Add desktop actions as tools to AI agents in AI Agent Studio.
-   Enable AI agents to interact with legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.
-   Monitor desktop actions being executed by AI agents in Execution workspace in the Desktop-in-Desktop session.

 See [Agentic Desktop](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Record desktop actions more accurately by using the new AI-powered recording mode when creating desktop actions.
-   Save time on manual setup by letting AI automatically insert anchors and generate screen context for each captured screen and add desktop action description after recording.
-   Switch between AI-assisted recording and manual recording by using the new **Record with AI \(recommended\)** check box that replaces the previous capture modes in the Create Desktop Action dialog.
-   Make desktop actions more flexible by configuring parameters for on-screen task desktop actions.
-   Pass dynamic values at runtime by mapping parameters in the Map parameters section in AI Agent Studio.
-   Control data visibility and security by using the **Shared** and **Mark As Sensitive** fields on the Desktop action parameter form.
-   Get a quick guidance on how to effectively use the recorder with the recorder tips modal.
-   Keep browser tabs open after an adaptive desktop action completes by using the **sn\_naa.keep\_tab\_open** system property. The property is enabled by default.
-   Use the enhanced adaptive desktop actions to improve execution efficiency.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   The name of the application is now changed to AI Desktop Actions from Agentic Desktop.
-   Use the desktop action to automate dynamic steps that are determined by AI, and automating the recorded steps.
-   Get a quick overview of the AI Desktop Actions application by using the onboarding wizard that highlights steps related to recording, refining, testing, and activating desktop actions.
-   Use the **Show Inputs** / **Show All** buttons in the Test modal to filter required input fields.
-   Use the latest LLM version for improved performance.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Improved error and informational messages for better guidance and troubleshooting.
-   Added a **Delete** button to the image canvas to remove a screen.
-   Enabled screen-level testing while designing desktop actions.

 See [Agentic Desktop](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

