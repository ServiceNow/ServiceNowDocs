---
title: ServiceNow Arc release notes
description: The ServiceNow Arc application is a desktop AI agent that plans and runs multistep tasks across your enterprise applications within the governance and security policies your administrators define. See the following sections for release notes by version.ServiceNow Arc is now available, with a choice of AI models, connectors, MCP servers, skill and sub-agents all governed by policies, tiered approvals and Auto Mode, and usage insights and analytics.ServiceNow Arc now runs on Windows, builds ServiceNow apps with Fluent, and brings policy authoring into AI Control Tower. This release also adds notifications for approvals and reminders and MCP servers managed by administrators, and improves auto mode, schedules, Microsoft 365 connector permissions, approvals, and error messages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/servicenow-cowork-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-27"
reading_time_minutes: 9
keywords: [ServiceNow Cowork release notes, Cowork release notes, ServiceNow Arc release notes, Arc release notes]
breadcrumb: [AI Experiences release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Arc release notes

The ServiceNow Arc application is a desktop AI agent that plans and runs multistep tasks across your enterprise applications within the governance and security policies your administrators define. See the following sections for release notes by version.

## About ServiceNow Arc

-   Delegate multistep work to an AI agent on your desktop that works alongside the applications you already use.
-   Control agent autonomy with tiered approval gates, priority based policies, and administrator governance of MCP servers.
-   Choose from Anthropic Claude, OpenAI GPT, and Google Gemini models through Generative AI Controller.
-   Extend the agent with skills, and track adoption and policy activity in Usage Insights.
-   Schedule recurring tasks and reminders from chat or the Schedules view, starting from ready made blueprints.

See ServiceNow Arc for more information.

## Activation and other requirements

**Note:** ServiceNow Arc is available in the ServiceNow Store. For details, see the activation information below.

-   **Activation information**

    Install ServiceNow Arc by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    The desktop app runs on macOS computers with Apple silicon or Intel processors, and on Windows computers.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/intelligent-experiences-rn-landing.md)

## Version 1.0.0

ServiceNow Arc is now available, with a choice of AI models, connectors, MCP servers, skill and sub-agents all governed by policies, tiered approvals and Auto Mode, and usage insights and analytics.

### What's new

-   **Microsoft 365 and GitHub connectors**

    Connect ServiceNow Arc to Microsoft 365 and GitHub so the agent can work with your mail, calendar, files, and repositories. Administrators control which connector operations the agent can perform through connector scopes.

-   **Sandboxed execution**

    The agent runs scripts and commands in an isolated virtual machine sandbox on the Mac, with access to the files you share. The sandbox image comes from your connected instance, so updates to it apply the next time you launch, sign in, or switch instances.

-   **Policy management and governance in ServiceNow Arc**

    Control what the agent can reach and change with network allowlists, sandbox rules, file type rules, and connector scopes, alongside tool gates and approval patterns. Target each policy to specific users and groups with user criteria. The Default Policy applies to everyone, and clients keep enforcing their last policy if the instance is unreachable. Override the Default Policy by creating a policy with a higher priority. The policy with the lowest priority number wins, and when priorities tie, the most restrictive rule wins. The same resolution applies to tool gates, connector scopes, and capability overrides. Tool gates offer an auto approval option alongside Allow, Deny, and require approval.

-   **Tiered approvals and Auto Mode**

    Assign each approval pattern a hard gate or a soft gate. Hard asks for approval every time, with **Allow**, and **Deny** options. Soft gates add an **Always allow** option that persists across sessions. Users can review and revoke these grants from the **Approvals** list in Settings.

    To reduce prompts, administrators turn on the Auto Approval capability \(**auto\_approval**, off by default\), an AI classifier evaluates soft gate and unmatched tool calls against the user's goal and either proceeds or asks for approval. Hard gates never auto-approve. If the classifier is unavailable, soft gate and unmatched calls proceed, and every classifier and fallback decision is logged.

-   **Priority-based policy resolution**

    Override the default policy by creating a policy with a lower priority number. The lowest priority number wins. When priorities tie, the approval pattern with the more specific match wins, and then the more restrictive rule. The same resolution applies to all policy components, including tool gates, connector scopes, and capability overrides. Tool gates offer Allow, Deny, HITL, and Auto.

-   **Approval pattern Match Mode**

    Define how an approval pattern matches commands with a single Match Mode field: **Exact**, **Relaxed**, or **Keyword**. Keyword mode requires a tool filter and matches whole words only. Write verbs for the bash tool live in a Keyword approval pattern instead of the bash tool gate. Commands that read credential paths or set sensitive environment variables require approval.

-   **Skills catalog and slash commands**

    Browse skills by source \(Default or Custom\), invocation \(agent invoked or user invoked\), and connector, and see whether each skill's required connector is connected. User invoked skill has a unique slash command; typing it in the composer expands the skill's instructions before you send.

    Create custom skills by adding a folder with a SKILL.md file, or let the agent create them from a conversation. When a skill script fails, the agent diagnoses and detects the error, applies a correction to fix it, and retries.

-   **Bundled skills**

    ServiceNow Arc ships with a focused set of default skills, including separate skills for ServiceNow, Microsoft 365, planning and meeting skills.

-   **Usage Insights analytics**

    View ServiceNow Arc as an application in Usage Insights, with active users, monthly and daily active users, and sessions. Report on conversations by how they start, success and error rates, user interventions, and the model used, along with connector, MCP, and policy block events.

    Build funnels, cohorts, and retention reports, and drill down from aggregate charts to individual users and tasks. Data is scoped to your instance only, and user IDs are hashed.

-   **Observability in AI Control Tower**

    Register ServiceNow Arc as a managed AI system in AI Control Tower to monitor its use across your organization. Sessions and traces flow into AI Control Tower, where each trace receives quality, safety, and risk assessment scores. You can drill down from a session to its individual steps, including tool calls and policy decisions.

-   **Kill switch and heartbeat monitoring in AI Control Tower**

    Monitor and control ServiceNow Arc across your organization from AI Control Tower. The fleet view shows who installs ServiceNow Arc and who is active. Heartbeat monitoring checks each installation at regular intervals and flags any that stop responding, so you can find offline installations before they affect users. If an agent takes unsafe actions, use the kill switch to stop them from escalating. The kill switch revokes credentials and terminates running actions.

-   **Predictable retry behavior**

    The agent stops and reports the problem after a bounded number of attempts on the same task, instead of retrying indefinitely or working around a policy block. When a policy blocks an action, the agent reports the block and the reason and makes no further attempts.

-   **Automatic app updates**

    The app checks for updates at start-up, during onboarding, every 30 minutes, and on demand from Settings. A required update shows an Update and Restart screen; updates found in the background appear as a dismissible notification. Each update is signature verified before it installs.

-   **Model choice acrossAnthropic Claude, GPT, and Google Gemini**

    Choose a model from Anthropic Claude \(Opus 4.6, 4.7, 4.8, and Sonnet 4.6\), OpenAI GPT \(5.4 and 5.5\), and Google Gemini \(3.5 Flash\), all routed through Generative AI Controller. After you connect, the model list comes from the models configured on your instance. Opus 4.8 is the default.

-   **Assist metering and entitlements**

    User initiated requests consumes assists, recorded in the generative AI log under the feature name ServiceNow Arc Execution. Check your entitlements to determine whether you have access to ServiceNow Arc.


### Plugin information

-   **New plugins**

    ServiceNow Arc \(sn\_app\_cowork\): Provides the Arc policy, approval, and configuration records that govern the desktop agent.


## Version 1.1.2

ServiceNow Arc now runs on Windows, builds ServiceNow apps with Fluent, and brings policy authoring into AI Control Tower. This release also adds notifications for approvals and reminders and MCP servers managed by administrators, and improves auto mode, schedules, Microsoft 365 connector permissions, approvals, and error messages.

### What's new

-   **Windows support**

    ServiceNow Arc now supports Windows. On Windows desktop, the Arc application acts as an AI agent that plans and runs multi-step tasks across your enterprise applications, within the governance and security policies your administrators define.

-   **Arc policies in AI Control Tower**

    Administrators author and manage ServiceNow Arc agent policies in AI Control Tower, on the **Arc policies** tab under **Govern** &gt; **Policies**.

-   **MCP servers managed by administrators**

    MCP server connectors that administrators configure on the instance appear in ServiceNow Arc ready to connect, so users don't enter a server URL or client ID.

    When an administrator deactivates a connector, Arc ends any active session, blocks reconnection, and tells the user why. After the connector is reactivated, users reconnect it themselves.

-   **Notifications for approvals and reminders**

    ServiceNow Arc notifies users about pending approvals and reminders, with one notification for each pending approval before it times out. When users are in another chat, a banner appears at the top of the Arc window. When they're in another app, a desktop notification appears. Users can approve or reject the action from either one.

    For more information, see Turn notifications on or off.

-   **Fluent app development for MacOs**

    Build, deploy, and edit ServiceNow scoped applications from a conversation in ServiceNow Arc, using the Now SDK, which is preinstalled in the sandbox. The agent presents a build plan for approval, then creates a TypeScript project and authors the data model, server and client logic, flows, UI, AI agents, and tests.

    App development isn't supported on Windows.

-   **File preview**

    Users can preview Word, Excel, PowerPoint, PDF, and PNG files in ServiceNow Arc. From the preview, they can download a file, open it in its native app or its folder, zoom in or out, and view it full screen.


### What's changed

-   **Auto mode for each chat**

    Users choose **Standard** or **Auto** approval for each chat in ServiceNow Arc from the message box, and set a default approval mode in **Settings** &gt; **Approvals** for new chats and background runs, such as scheduled tasks.

    To make auto mode available, administrators turn on the Auto Mode capability \(**auto\_approval**\), which is off by default, and set tool gates to **Auto Approval** for the tools that auto mode can cover.

-   **Microsoft 365 connector permissions**

    Users set each Microsoft 365 connector capability to **Allow**, **Ask me first**, or **Deny**. With **Ask me first**, an approval card asks the user to allow or deny the action every time it runs, and auto mode never skips it.

    Administrators set the upper limit with the **Approval gate** field on each connector scope in a policy. Users can choose only a stricter setting, and capabilities the policy limits show **Set by your organization**. Microsoft 365 scopes turned off on the instance now appear in the list. Existing policies keep their behavior, and the audit log records policy changes and Microsoft 365 write actions.

-   **Clearer approvals**

    Approval cards in ServiceNow Arc now name the action and describe what's at stake, such as what the action changes or sends and whether it can be undone. For a command under a hard gate, the card names the command that triggered it.

    **Allow always** is renamed **Always Allow**, and standing approvals in **Settings** &gt; **Approvals** describe the whole group of actions they cover.

    Accessing a folder outside the workspace asks for approval with a soft gate that offers **Always Allow**, unless an approval pattern in the policy applies a hard gate to that call.

-   **Schedules management**

    Users create scheduled tasks from **Schedules** in the ServiceNow Arc sidebar or through chat. They can start from a blueprint or a custom reminder, and select **Reminder only** to get a notification instead of running a task.

    The list shows every schedule, whether created in chat or in **Schedules**. Users can search the list, run, duplicate, edit, pause, or delete any schedule, and see when it last ran and when it runs next.


