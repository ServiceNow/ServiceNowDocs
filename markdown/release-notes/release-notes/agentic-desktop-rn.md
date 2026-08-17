---
title: AI Desktop Actions release notes
description: The ServiceNow AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-31"
reading_time_minutes: 15
---

# AI Desktop Actions release notes

The ServiceNow® AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions is a new application in the Zurich release.

## AI Desktop Actions highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

-   ServiceNow Otto is the new AI experience brand. ServiceNow Now Assist is now ServiceNow Otto.
-   Preserve context across long-running sessions by summarizing older step history instead of discarding it.
-   Three new system properties are included to manage the compaction feature.
-   Adaptive desktop actions are now batched for better performance. Multiple actions execute per LLM call instead of one call per action that reduces the round-trip latency that previously limited production readiness.

[Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)

-   Use the unified automation creation journey that spans seamlessly across Task Mining, Automation Center, and AI Agent Studio eliminating context switching and streamlining automation development.
-   Automatically generate desktop actions from real user task patterns captured by using Task Mining.
-   Automatically create an AI agent from desktop actions context from Automation Center.

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   Record desktop actions more accurately by using the new AI-powered recording mode when creating desktop actions.
-   Save time on manual setup by letting AI automatically insert anchors and generate screen context for each captured screen and add desktop action description after recording.
-   Switch between AI-assisted recording and manual recording by using the new **Record with AI \(recommended\)** check box that replaces the previous capture modes in the Create Desktop Action dialog.
-   Make desktop actions more flexible by configuring parameters for on-screen task desktop actions.
-   Pass dynamic values at runtime by mapping parameters in the Map parameters section in AI Agent Studio.
-   Control data visibility and security by using the **Shared** and **Mark As Sensitive** fields on the Desktop action parameter form.
-   Get a quick guidance on how to effectively use the recorder with the recorder tips modal.
-   Keep browser tabs open after an adaptive desktop action completes by using the **sn\_naa.keep\_tab\_open** system property. The property is enabled by default.
-   Use the enhanced adaptive desktop actions to improve execution efficiency.

[Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)

-   The name of the application is now changed to AI Desktop Actions from Agentic Desktop.
-   Use the desktop action to automate dynamic steps that are determined by AI, and automating the recorded steps.
-   Get a quick overview of the AI Desktop Actions application by using the onboarding wizard that highlights steps related to recording, refining, testing, and activating desktop actions.
-   Use the **Show Inputs** / **Show All** buttons in the Test modal to filter required input fields.
-   Use the latest LLM version for improved performance.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Improved error and informational messages for better guidance and troubleshooting.
-   Added a **Delete** button to the image canvas to remove a screen.
-   Enabled screen-level testing while designing desktop actions.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Use smart sizing in the Execution workspace with the **Fit to window** and **Original resolution** options.
-   Enable AI agents to securely access SSH parameters by setting up parameter records in the ServiceNow instance.
-   Test specific screens within desktop actions without running the entire flow.
-   Access application controls during recording with a recorder toolbar.
-   Configure the AI Desktop Actions installer experience for settings that are essential for seamless execution of desktop actions.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Desktop actions now run reliably on machines with different screen resolutions.

-   Design desktop actions of type UI block \(UI actions\) by capturing user interactions, adding details, and activating them in Design workspace.
-   Use default desktop actions of type non-UI block \(non-UI actions\) that include pre-built connectors to interact with various applications and system components.
-   Add desktop actions as tools to AI agents in AI Agent Studio.
-   Enable AI agents to interact with legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.
-   Monitor desktop actions being executed by AI agents in Execution workspace in the Desktop-in-Desktop session.

See [AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-landing-page.md) for more information.

## Important information for upgrading AI Desktop Actions to Zurich

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

## AI Desktop Actions features

-   **[Preserve context across long-running sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-ai-wa-access-using-nap.md)**

    Preserve context across long-running sessions by summarizing older step history instead of discarding it. When history exceeds the configured window, older steps are automatically summarized instead of being discarded. They preserve context about earlier actions, failed approaches, and application state.

-   **[New system properties introduced to manage compaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/components-installed-with-agentic-desktop.md)**

    Three new system properties are included to manage the compaction feature:

    |Property|Type|Default|Purpose|
    |--------|----|-------|-------|
    |sn\_naa.web\_agent.compaction\_enabled|true \| false|true|Enables summarization of steps that exceed the history limit, rather than discarding them. When turned off, only the most recent configured number of steps are retained.|
    |sn\_naa.web\_agent.compaction\_history\_limit|Integer|15|Sets the maximum number of unsummarized steps allowed before the oldest batch is summarized. When unsummarized steps exceed this value, compaction is triggered.|
    |sn\_naa.web\_agent.summarization\_batch\_size|Integer|10|Sets the number of steps combined into a single summary. Larger batches reduce how often summarization runs, but produce less granular summaries.|


-   **[Unified automation workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/explore-agentic-desktop.md)**

    Use the unified automation creation journey that eliminates manual intervention and saves time.

    -   Request automations from Task Mining to automate desktop activities collected by the Task Mining agent.
    -   Generate automations in Automation Center to create on-screen and background desktop actions.
    -   From Automation Center, automatically create an AI agent that uses these desktop action tools.
    -   Test and deploy the AI agent in AI Agent Studio.

-   **[Record desktop actions with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/record-with-ai-ad.md)**

    -   Record on-screen task desktop actions using AI to automatically validate anchor positions and generate screen contexts at design time, reducing automation failures caused by fragile anchors at testing or runtime.
    -   Use a new role, sn\_desktop\_core.desktop\_action\_user that enables users to record desktop action with AI.
    -   Enable AI to analyze the recording in three stages: analyzing the recording, inserting anchors, and generating screen contexts by selecting **Record with AI \(recommended\)** in the **Create Desktop Action** dialog and finish recording.
    -   Identify AI-generated anchors and screen contexts that are marked with an AI badge in the properties panel. Each screen includes an editable screen context that helps AI agents understand the screen's intent at runtime.
    -   Regenerate screen context and anchor positions that don't meet your expectations by selecting **Retry** in the screen properties panel.
    -   Resolve anchor issues before activation by responding to the alert that appears when any screens have failed anchors in a desktop action recorded with AI.
    -   Reduce manual setup time by letting AI auto-fill the desktop action intent in the **Action description** field when you select the **Record with AI** option. An AI badge confirms that the description was filled by AI.
    -   Control whether **Record with AI** is the default recording option by configuring the new **sn\_desktop\_core.record\_with\_ai** property. By default, its value is set to true.
    **Important:** Record with AI requires the ServiceNow AI Lens skill to be active and you must have the sn\_desktop\_core.desktop\_action\_user role. If any of these conditions is not met, the **Record with AI** option is unavailable. You can still create desktop actions using auto-capture mode. Contact your ServiceNow administrator to enable these settings.

-   **[Configure parameters for dynamic values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-parameter-record-ad.md)**

    -   Provide dynamic values, such as credentials and user-specific inputs to on-screen task desktop actions by creating Desktop action parameter records in your ServiceNow instance.
    -   Make a single stored parameter value available to all users by selecting the **Shared** field on a parameter record. When **Shared** is selected, the agent uses the one associated parameter value record, regardless of which user triggered the agent. Only a user with the sn\_aia.admin role can create the parameter value record for a shared parameter.
    -   Encrypt all associated parameter value records by selecting the **Mark As Sensitive** field on a parameter record. The agent decrypts the value at execution time. For non-sensitive parameters, the value is passed to the agent as plain text.
    -   In the AI Desktop Actions client application, enable the Set Text and Send Keys step types to use parameters by selecting the **Use parameter** property.
    -   In AI Agent Studio, when you add an on-screen task desktop action tool that contains inputs configured for parameters, the **Map parameters** section appears. You can map inputs of on-screen task desktop actions to parameter records. These parameter values aren't exposed in agent instructions. Select a parameter record for each input to define the value the AI agent uses when executing the desktop action.
    **Important:**

    The **Shared** and **Mark As Sensitive** fields can only be modified when no Desktop action parameter value records exist under the parameter record.


-   **[Use the new application name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-landing-page.md)**

    The product formerly referred to as Agentic Desktop has been rebranded as AI Desktop Actions. All UI labels, navigation elements, and in-product text updated to reflect the new name.

-   **[Automate dynamic steps with desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/web-agents-overview.md)**
    -   Use the desktop action to automate dynamic steps that are determined by AI during execution.
    -   Install the **ServiceNow Web Automation** chrome extension for AI agent to interact with web applications.
    -   Use the default Web Automation Agent AI agent and Web Automation agentic workflow to automate repetitive tasks.
    -   See every click, keystroke, and scroll your AI agent makes in real time, with consent prompts before execution kicks off and timely warnings before your session expires.
    -   Pause a running AI agent, provide corrective input, and resume. The AI agent replans based on your instructions, keeping execution on the right track.
-   **[Use the onboarding wizard to get the app overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/desktop-actions.md)**

    Get a quick overview of the application by using the onboarding wizard that highlights recording, refining, testing, and activating desktop actions.

    Select **Skip intro** to bypass the onboarding wizard and go to the home page. Select the **Don't show this again** option to prevent the wizard from appearing the next time you open the app. After completing the onboarding wizard, select **Get started** to start creating desktop actions.

-   **[Filter required inputs for testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/test-activate-desktop-action-ad.md)**

    Use filtering options to filter the inputs that are required.

    -   **Show Inputs** — Filters the screens with required input fields.
    -   **Show All** — Removes the filter and displays all screens.

-   **[Improved error and informational messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/test-activate-desktop-action-ad.md)**

    Improved error and informational messages for better guidance and troubleshooting during testing of desktop actions.

-   **[Delete button on image canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-overview.md)**

    Added a **Delete** button to the image canvas to remove a screen.

-   **[Test button for a screen in the Design tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-overview.md)**

    Test screens directly from the design tab while designing desktop actions.


-   **[Smart sizing in the Execution workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-excution-workspace.md)**

    Smart sizing is now supported in the Execution Workspace with **Fit to window** and **Original resolution** options. The **Original resolution** option allows you to access different areas of the captured screen more easily.

    -   **Fit to window**: Automatically scales the desktop session to fit within the Execution Workspace while keeping it fully visible and readable.
    -   **Original resolution**: Displays the desktop session at its original resolution. Scroll bars appear if the desktop session is larger than the Execution workspace.
-   **[Recorder enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/action-recorder-ad.md)**
    -   The recorder toolbar is now floating, making it easier to access application controls during recording.
    -   The recorder now adds only one screen per unique window during recording by auto-merging and optimizing duplicate screens.
    -   You can capture maximum of 50 steps using the recorder in a recording session. While auto-capturing steps, a counter now displays the remaining number of steps you can record using the recorder \(for example, “35 of 50 max”\).
-   **[Screen-level testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/test-activate-desktop-action-ad.md)**
    -   Quickly isolate and troubleshoot issues by testing a specific screen within desktop actions without running the entire flow.
    -   While working on a desktop action, the test values you enter are retained across test runs until you close the desktop action or reset the test values.
-   **[View list of existing desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/desktop-actions-designer-workspace-ad.md)**
    -   View list of all existing desktop actions in the Desktop Action module in the ServiceNow instance. View related lists that include Desktop Action application, AI Agents, and Desktop action executions for UI block, and AI Agents and Desktop action executions for non-UI block.
-   **[Improved AI Desktop Actions installer experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/download-agentic-desktop-installer.md)**

    The installer now guides you through the following two configurations that are essential for seamless execution of desktop actions:

    -   Option to automatically add the current user to the Windows Remote User group
    -   Configuration that validates if required .NET Desktop Runtime is installed or not. If not installed, provides a link to download and install the same.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Support for different screen resolutions and scaling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-overview.md)**

    Desktop actions now run reliably on machines with different screen resolutions and scaling. Screen resolution and scaling are consistent across all screens of a desktop actions during creation, saving, and publishing.


-   **[Design UI block desktop actions in Design workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-overview.md)**

    Design, configure, and manage desktop actions in the Design workspace that enables:

    -   Auto-recording or manually capturing screens and defining UI interactions, such as clicking buttons, typing into text boxes, and selecting from drop-down menus.
    -   Adding details such as name, description, input and output parameters.
    -   Testing desktop actions before activating them.
    -   Publishing desktop actions to AI Agent Studio as tools for AI agents to execute.
    Example: Filling out fields and submitting a form.

-   **[Use non-UI block desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/desktop-actions-designer-workspace-ad.md)**

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

-   **[Adding desktop actions to AI agents in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-ai-agents-ad.md)**

    Seamless integration with AI Agent Studio has enabled effortless configuration of desktop actions to automate repetitive tasks on applications without APIs. AI agents can reason, plan, and execute desktop actions autonomously and semi-autonomously across legacy systems and desktop applications without complex setups.

-   **[Monitor desktop actions in Execution workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/use-agentic-desktop.md)**

    Trigger desktop actions from the Now Assist panel that are executed by AI agents in the Execution workspace. Interact with the automation when human input is required. These automations run in the background and listen for instructions dispatched from the ServiceNow instance. You can continue working on other desktop applications outside Execution workspace.

-   **[Leverage core desktop capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/desktop-actions-designer-workspace-ad.md)**

    Automate form filling, application clicks, and Windows OS file handling. Create workflows across legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.


## Changed in this release

-   **[Renamed ServiceNow AI experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-desktop-landing-page.md)**

    ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI Desktop Actions. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


## Activation information

AI Desktop Actions is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-agentic-desktop.md).

## Additional requirements

The following are required to use AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install ServiceNow Otto AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-ai-agents-plugins.md).

You must enable Next Experience UI Framework before you can use the Now Assist panel.

## Browser requirements

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

## Related ServiceNow applications and features

-   **[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-ai-agents.md)**

    The ServiceNow® Now Assist AI agents are entities that mimic human-like intelligence by using large language models \(LLMs\). AI agents can perform tasks that range from simple automated responses to complex problem solving. By using AI agents, you can reduce the workloads of your live agents and help increase their productivity.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    With the ServiceNow®Now Assist panel, you can get assistance from generative AI experiences to solve customer issues fast. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information quickly.

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLMs with your workflows.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

