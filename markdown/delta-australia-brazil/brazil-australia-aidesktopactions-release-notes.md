---
title: Combined AI Desktop Actions release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for AI Desktop Actions from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-aidesktopactions-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined AI Desktop Actions release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for AI Desktop Actions from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Desktop Actions release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Desktop Actions to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download installer](https://www.servicenow.com/docs/access?context=download-agentic-desktop-installer&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download installer](https://www.servicenow.com/docs/access?context=download-agentic-desktop-installer&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for AI Desktop Actions.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Execute adaptive desktop actions on macOS](https://www.servicenow.com/docs/access?context=ai_desktop_actions_adaptive&family=australia&ft:locale=en-US)**

Download the new AI Desktop Actions installer for macOS with M-series processor support \(ARM64 architecture\). The adaptive desktop actions enable AI agents to navigate applications and browsers and perform tasks on macOS systems. Both adaptive and defined desktop actions are now available with platform-specific installers.

    -   Review the AI agent's execution plan before it runs and pause execution to make manual adjustments at any time.
    -   Explicit user consent is required before the AI agent can access desktop, third-party services, and files.
    -   Monitor the live execution of adaptive desktop actions in the preview window.
    -   Refer the real-time status tracking that shows whether the AI agent is initiating, running, or paused.
    -   Take control of the execution where your input is needed.
    -   The AI agent batches consecutive actions into single execution calls where possible, minimizing round trips and reducing overall execution time.
-   **[Control resource access using policy and rules](https://www.servicenow.com/docs/access?context=security_policy_governance_concept&family=australia&ft:locale=en-US)**

Create policies and rules to control which resources AI agents can access.

    -   Policies: Collection of resource access rules that applies to a specific user group or set of users based on defined user criteria.
    -   Resource access rules: Specific restrictions controlling agent access to various resource types, such as files, folders, websites, and applications.
    -   Bi-directional policy-rule mapping: Link policies to rules from either the policy record or the rule record, enabling rule reuse across multiple policies.
-   **[Credential and dynamic parameter management](https://www.servicenow.com/docs/access?context=credential-storage&family=australia&ft:locale=en-US)**

Reference credentials or other user-specific values by name in your instructions. The agent resolves them securely at execution time, so you never have to type them in yourself.

-   **[File upload and download](https://www.servicenow.com/docs/access?context=upload-download-file&family=australia&ft:locale=en-US)**

Upload files to web forms and track file downloads during automated browser tasks. The agent validates file safety, confirms the target field with the reasoning model, and escalates to the user when it can't proceed safely.


 -   **[Preserve context across long-running sessions](https://www.servicenow.com/docs/access?context=na-ai-wa-access-using-nap&family=australia&ft:locale=en-US)**

Preserve context across long-running sessions by summarizing older step history instead of discarding it. When history exceeds the configured window, older steps are automatically summarized instead of being discarded. They preserve context about earlier actions, failed approaches, and application state.

-   **[New system properties introduced to manage compaction](https://www.servicenow.com/docs/access?context=components-installed-with-agentic-desktop&family=australia&ft:locale=en-US)**

Three new system properties are included to manage the compaction feature:

    |Property|Type|Default|Purpose|
    |--------|----|-------|-------|
    |sn\_naa.web\_agent.compaction\_enabled|true \| false|true|Enables summarization of steps that exceed the history limit, rather than discarding them. When turned off, only the most recent configured number of steps are retained.|
    |sn\_naa.web\_agent.compaction\_history\_limit|Integer|15|Sets the maximum number of unsummarized steps allowed before the oldest batch is summarized. When unsummarized steps exceed this value, compaction is triggered.|
    |sn\_naa.web\_agent.summarization\_batch\_size|Integer|10|Sets the number of steps combined into a single summary. Larger batches reduce how often summarization runs, but produce less granular summaries.|


 -   **[Unified automation workflow](https://www.servicenow.com/docs/access?context=explore-agentic-desktop&family=australia&ft:locale=en-US)**

Use the unified automation creation journey that eliminates manual intervention and saves time.

    -   Request automations from Task Mining to automate desktop activities collected by the Task Mining agent.
    -   Generate automations in Automation Center to create on-screen and background desktop actions.
    -   From Automation Center, automatically create an AI agent that uses these desktop action tools.
    -   Test and deploy the AI agent in AI Agent Studio.

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


</td></tr><tr><td>

Brazil

</td><td>

-   **[Execute adaptive desktop actions on macOS](https://www.servicenow.com/docs/access?context=ai_desktop_actions_adaptive&family=brazil&ft:locale=en-US)**

Download the new AI Desktop Actions installer for macOS with M-series processor support \(ARM64 architecture\). The adaptive desktop actions enable AI agents to navigate applications and browsers and perform tasks on macOS systems. Both adaptive and defined desktop actions are now available with platform-specific installers.

    -   Review the AI agent's execution plan before it runs and pause execution to make manual adjustments at any time.
    -   Explicit user consent is required before the AI agent can access desktop, third-party services, and files.
    -   Monitor the live execution of adaptive desktop actions in the preview window.
    -   Refer the real-time status tracking that shows whether the AI agent is initiating, running, or paused.
    -   Take control of the execution where your input is needed.
    -   The AI agent batches consecutive actions into single execution calls where possible, minimizing round trips and reducing overall execution time.
-   **[Control resource access using policy and rules](https://www.servicenow.com/docs/access?context=security_policy_governance_concept&family=brazil&ft:locale=en-US)**

Create policies and rules to control which resources AI agents can access.

    -   Policies: Collection of resource access rules that applies to a specific user group or set of users based on defined user criteria.
    -   Resource access rules: Specific restrictions controlling agent access to various resource types, such as files, folders, websites, and applications.
    -   Bi-directional policy-rule mapping: Link policies to rules from either the policy record or the rule record, enabling rule reuse across multiple policies.
-   **[Credential and dynamic parameter management](https://www.servicenow.com/docs/access?context=credential-storage&family=brazil&ft:locale=en-US)**

Reference credentials or other user-specific values by name in your instructions. The agent resolves them securely at execution time, so you never have to type them in yourself.

-   **[File upload and download](https://www.servicenow.com/docs/access?context=upload-download-file&family=brazil&ft:locale=en-US)**

Upload files to web forms and track file downloads during automated browser tasks. The agent validates file safety, confirms the target field with the reasoning model, and escalates to the user when it can't proceed safely.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing AI Desktop Actions features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Browser startup and tab behavior](https://www.servicenow.com/docs/access?context=na-ai-wa-access-using-nap&family=australia&ft:locale=en-US)**

Browser session now opens to an empty page instead of Google's homepage. Automation actions within the same chat window now reuse the existing browser tab instead of opening a new tab for every action. A new tab opens only when a new chat session starts or you close the current tab.

-   **[Improved security for adaptive desktop actions system properties](https://www.servicenow.com/docs/access?context=components-installed-with-agentic-desktop&family=australia&ft:locale=en-US)**

Adaptive desktop actions system properties now require appropriate read and write roles. This change prevents unauthorized users from viewing or modifying the configuration settings, while automation continues to work as expected.


 -   **[Renamed ServiceNow AI experience](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=australia&ft:locale=en-US)**

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI Desktop Actions. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


 The system now suggests a full URL instead of a partial URL. For example, `https://<instance name>.servicenow.com`.

 Pagination is implemented for desktop actions on the AI Desktop Actions home page, which helps improve navigation and load times.

 -   **[Optional Application name field](https://www.servicenow.com/docs/access?context=add-details-desktop-action-ad&family=australia&ft:locale=en-US)**

The Application field in the Details tab is now optional, enabling you to save and run desktop actions without entering an application name.

-   **[Improved connectors descriptions for non-UI block desktop actions](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&family=australia&ft:locale=en-US)**

Descriptions for Excel, Word, PDF, and System Actions connectors are enhanced to improve accuracy and selection.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Browser startup and tab behavior](https://www.servicenow.com/docs/access?context=na-ai-wa-access-using-nap&family=brazil&ft:locale=en-US)**

Browser session now opens to an empty page instead of Google's homepage. Automation actions within the same chat window now reuse the existing browser tab instead of opening a new tab for every action. A new tab opens only when a new chat session starts or you close the current tab.

-   **[Improved security for adaptive desktop actions system properties](https://www.servicenow.com/docs/access?context=components-installed-with-agentic-desktop&family=brazil&ft:locale=en-US)**

Adaptive desktop actions system properties now require appropriate read and write roles. This change prevents unauthorized users from viewing or modifying the configuration settings, while automation continues to work as expected.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some AI Desktop Actions features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some AI Desktop Actions features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

AI Desktop Actions is available with activation of any ServiceNow Otto plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure](https://www.servicenow.com/docs/access?context=configure-agentic-desktop&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

AI Desktop Actions is available with activation of any ServiceNow Otto plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure](https://www.servicenow.com/docs/access?context=configure-agentic-desktop&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Desktop Actions we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Additional requirements**

The following are required to use defined AI Desktop Actions:

    -   Operating system: Microsoft Windows 11.
    -   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
    -   No extended monitors are connected.
To use adaptive desktop actions, Web Automation Chrome browser extension is required for web and AI Desktop Actions for macOS is required for desktop and web.

You must first install the supported ServiceNow Otto version of ServiceNow to be able to use the ServiceNow Otto AI agents. For more information, see [Install ServiceNow Otto AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=australia&ft:locale=en-US).

You must enable Next Experience UI Framework before you can use the ServiceNow Otto panel.


</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**

The following are required to use defined AI Desktop Actions:

    -   Operating system: Microsoft Windows 11.
    -   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
    -   No extended monitors are connected.
To use adaptive desktop actions, Web Automation Chrome browser extension is required for web and AI Desktop Actions for macOS is required for desktop and web.

You must first install the supported ServiceNow Otto version of ServiceNow to be able to use the ServiceNow Otto AI agents. For more information, see [Install ServiceNow Otto AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=brazil&ft:locale=en-US).

You must enable Next Experience UI Framework before you can use the ServiceNow Otto panel.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Desktop Actions we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Browser requirements**

ServiceNow Otto AI agents support various browsers, including Google Chrome and Microsoft Edge. ServiceNow Otto AI agents aren't supported in Internet Explorer.


</td></tr><tr><td>

Brazil

</td><td>

-   **Browser requirements**

ServiceNow Otto AI agents support various browsers, including Google Chrome and Microsoft Edge. ServiceNow Otto AI agents aren't supported in Internet Explorer.


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Desktop Actions, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   Automate multi-step desktop and web tasks that involve conditional logic, freeing your users to focus on work that needs a human touch.
-   Adapt to changes in application state and UI in real-time, reducing the need to maintain rigid scripts.
-   Detect errors during execution and recover by evaluating context and trying alternative approaches.
-   Let AI agents process instructions and generate execution plans autonomously or semi-autonomously, reducing manual setup for repetitive tasks.

 See [Agentic Desktop](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Automate multi-step desktop and web tasks that involve conditional logic, freeing your users to focus on work that needs a human touch.
-   Adapt to changes in application state and UI in real-time, reducing the need to maintain rigid scripts.
-   Detect errors during execution and recover by evaluating context and trying alternative approaches.
-   Let AI agents process instructions and generate execution plans autonomously or semi-autonomously, reducing manual setup for repetitive tasks.

 See [Agentic Desktop](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

