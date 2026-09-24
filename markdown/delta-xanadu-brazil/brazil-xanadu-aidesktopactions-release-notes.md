---
title: Combined AI Desktop Actions release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for AI Desktop Actions from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-aidesktopactions-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined AI Desktop Actions release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for AI Desktop Actions from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Desktop Actions release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Desktop Actions to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download installer](https://www.servicenow.com/docs/access?context=download-agentic-desktop-installer&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Improved error and informational messages](https://www.servicenow.com/docs/access?context=test-activate-desktop-action-ad&family=zurich&ft:locale=en-US)**

Improved error and informational messages for better guidance and troubleshooting during testing of desktop actions.

-   **[Delete button on image canvas](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&family=zurich&ft:locale=en-US)**

Added a **Delete** button to the image canvas to remove a screen.

-   **[Test button for a screen in the Design tab](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&family=zurich&ft:locale=en-US)**

Test screens directly from the design tab while designing desktop actions.


</td></tr><tr><td>

Australia

</td><td>

-   **[Preserve context across long-running sessions](https://www.servicenow.com/docs/access?context=na-ai-wa-access-using-nap&family=australia&ft:locale=en-US)**

Preserve context across long-running sessions by summarizing older step history instead of discarding it. When history exceeds the configured window, older steps are automatically summarized instead of being discarded. They preserve context about earlier actions, failed approaches, and application state.

-   **[New system properties introduced to manage compaction](https://www.servicenow.com/docs/access?context=components-installed-with-agentic-desktop&family=australia&ft:locale=en-US)**

Three new system properties are included to manage the compaction feature:

    |Property|Type|Default|Purpose|
    |--------|----|-------|-------|
    |sn\_naa.web\_agent.compaction\_enabled|true \| false|true|Enables summarization of steps that exceed the history limit, rather than discarding them. When turned off, only the most recent configured number of steps are retained.|
    |sn\_naa.web\_agent.compaction\_history\_limit|Integer|15|Sets the maximum number of unsummarized steps allowed before the oldest batch is summarized. When unsummarized steps exceed this value, compaction is triggered.|
    |sn\_naa.web\_agent.summarization\_batch\_size|Integer|10|Sets the number of steps combined into a single summary. Larger batches reduce how often summarization runs, but produce less granular summaries.|


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Renamed ServiceNow AI experience](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=zurich&ft:locale=en-US)**

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI Desktop Actions. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


</td></tr><tr><td>

Australia

</td><td>

-   **[Renamed ServiceNow AI experience](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&family=australia&ft:locale=en-US)**

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI Desktop Actions. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

AI Desktop Actions is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure](https://www.servicenow.com/docs/access?context=configure-agentic-desktop&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Additional requirements**

The following are required to use AI Desktop Actions:

    -   Operating system: Microsoft Windows 11.
    -   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
    -   No extended monitors are connected.
You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install ServiceNow Otto AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).

You must enable Next Experience UI Framework before you can use the Now Assist panel.


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Browser requirements**

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. ServiceNow Now Assist is now ServiceNow Otto.
-   Preserve context across long-running sessions by summarizing older step history instead of discarding it.
-   Three new system properties are included to manage the compaction feature.
-   Adaptive desktop actions are now batched for better performance. Multiple actions execute per LLM call instead of one call per action that reduces the round-trip latency that previously limited production readiness.

 [Zurich Patch 11](https://www.servicenow.com/docs/access?context=zurich-patch-11&family=zurich&ft:locale=en-US)

-   Use the unified automation creation journey that spans seamlessly across Task Mining, Automation Center, and AI Agent Studio eliminating context switching and streamlining automation development.
-   Automatically generate desktop actions from real user task patterns captured by using Task Mining.
-   Automatically create an AI agent from desktop actions context from Automation Center.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

