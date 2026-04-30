---
title: AI Desktop Actions release notes
description: The ServiceNow AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-31"
reading_time_minutes: 7
---

# AI Desktop Actions release notes

The ServiceNow® AI Desktop Actions application enables you to design, configure, and manage desktop actions to automate repetitive tasks. These desktop actions are executed by AI agents created in AI Agent Studio. AI Desktop Actions is a new application in the Zurich release.

## AI Desktop Actions highlights for the Zurich release

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Improved error and informational messages for better guidance and troubleshooting.
-   Added a **Delete** button to the image canvas to remove a screen.
-   Enabled screen-level testing while designing desktop actions.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use smart sizing in the Execution workspace with the **Fit to window** and **Original resolution** options.
-   Enable AI agents to securely access SSH parameters by setting up parameter records in the ServiceNow instance.
-   Test specific screens within desktop actions without running the entire flow.
-   Access application controls during recording with a recorder toolbar.
-   Configure the AI Desktop Actions installer experience for settings that are essential for seamless execution of desktop actions.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Desktop actions now run reliably on machines with different screen resolutions.

-   Design desktop actions of type UI block \(UI actions\) by capturing user interactions, adding details, and activating them in Design workspace.
-   Use default desktop actions of type non-UI block \(non-UI actions\) that include pre-built connectors to interact with various applications and system components.
-   Add desktop actions as tools to AI agents in AI Agent Studio.
-   Enable AI agents to interact with legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.
-   Monitor desktop actions being executed by AI agents in Execution workspace in the Desktop-in-Desktop session.

See [AI Desktop Actions](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

## AI Desktop Actions features

-   **[Improved error and informational messages](https://www.servicenow.com/docs/access?context=test-activate-desktop-action-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Improved error and informational messages for better guidance and troubleshooting during testing of desktop actions.

-   **[Delete button on image canvas](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Added a **Delete** button to the image canvas to remove a screen.

-   **[Test button for a screen in the Design tab](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Test screens directly from the design tab while designing desktop actions.


-   **[Smart sizing in the Execution workspace](https://www.servicenow.com/docs/access?context=agentic-desktop-excution-workspace&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Smart sizing is now supported in the Execution Workspace with **Fit to window** and **Original resolution** options. The **Original resolution** option allows you to access different areas of the captured screen more easily.

    -   **Fit to window**: Automatically scales the desktop session to fit within the Execution Workspace while keeping it fully visible and readable.
    -   **Original resolution**: Displays the desktop session at its original resolution. Scroll bars appear if the desktop session is larger than the Execution workspace.
-   **[Recorder enhancements](https://www.servicenow.com/docs/access?context=action-recorder-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   The recorder toolbar is now floating, making it easier to access application controls during recording.
    -   The recorder now adds only one screen per unique window during recording by auto-merging and optimizing duplicate screens.
    -   You can capture maximum of 50 steps using the recorder in a recording session. While auto-capturing steps, a counter now displays the remaining number of steps you can record using the recorder \(for example, “35 of 50 max”\).
-   **[Screen-level testing](https://www.servicenow.com/docs/access?context=test-activate-desktop-action-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Quickly isolate and troubleshoot issues by testing a specific screen within desktop actions without running the entire flow.
    -   While working on a desktop action, the test values you enter are retained across test runs until you close the desktop action or reset the test values.
-   **View list of existing desktop actions**
    -   View list of all existing desktop actions in the Desktop Action module in the ServiceNow instance. View related lists that include Desktop Action application, AI Agents, and Desktop action executions for UI block, and AI Agents and Desktop action executions for non-UI block.
-   **[Improved AI Desktop Actions installer experience](https://www.servicenow.com/docs/access?context=download-agentic-desktop-installer&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The installer now guides you through the following two configurations that are essential for seamless execution of desktop actions:

    -   Option to automatically add the current user to the Windows Remote User group
    -   Configuration that validates if required .NET Desktop Runtime is installed or not. If not installed, provides a link to download and install the same.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Support for different screen resolutions and scaling](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Desktop actions now run reliably on machines with different screen resolutions and scaling. Screen resolution and scaling are consistent across all screens of a desktop actions during creation, saving, and publishing.


-   **[Design UI block desktop actions in Design workspace](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Design, configure, and manage desktop actions in the Design workspace that enables:

    -   Auto-recording or manually capturing screens and defining UI interactions, such as clicking buttons, typing into text boxes, and selecting from drop-down menus.
    -   Adding details such as name, description, input and output parameters.
    -   Testing desktop actions before activating them.
    -   Publishing desktop actions to AI Agent Studio as tools for AI agents to execute.
    Example: Filling out fields and submitting a form.

-   **[Use non-UI block desktop actions](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

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

-   **[Adding desktop actions to AI agents in AI Agent Studio](https://www.servicenow.com/docs/access?context=create-ai-agents-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Seamless integration with AI Agent Studio has enabled effortless configuration of desktop actions to automate repetitive tasks on applications without APIs. AI agents can reason, plan, and execute desktop actions autonomously and semi-autonomously across legacy systems and desktop applications without complex setups.

-   **[Monitor desktop actions in Execution workspace](https://www.servicenow.com/docs/access?context=use-agentic-desktop&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Trigger desktop actions from the Now Assist panel that are executed by AI agents in the Execution workspace. Interact with the automation when human input is required. These automations run in the background and listen for instructions dispatched from the ServiceNow instance. You can continue working on other desktop applications outside Execution workspace.

-   **[Leverage core desktop capabilities](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Automate form filling, application clicks, and Windows OS file handling. Create workflows across legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.


## Activation information

AI Desktop Actions is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using AI Desktop Actions, see [Configure AI Desktop Actions](https://www.servicenow.com/docs/access?context=configure-agentic-desktop&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Additional requirements

The following are required to use AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

You must enable Next Experience UI Framework before you can use the Now Assist panel.

## Browser requirements

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

## Related ServiceNow applications and features

-   **[Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Now Assist AI agents are entities that mimic human-like intelligence by using large language models \(LLMs\). AI agents can perform tasks that range from simple automated responses to complex problem solving. By using AI agents, you can reduce the workloads of your live agents and help increase their productivity.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    With the ServiceNow®Now Assist panel, you can get assistance from generative AI experiences to solve customer issues fast. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information quickly.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLMs with your workflows.


**Parent Topic:**[AI Experiences release notes](../analytics-intelligence-reporting/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

