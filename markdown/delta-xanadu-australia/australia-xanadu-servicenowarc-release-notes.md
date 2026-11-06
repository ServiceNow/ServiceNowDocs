---
title: Combined ServiceNow Arc release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow Arc from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/delta-xanadu-australia/australia-xanadu-servicenowarc-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 20
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Arc release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow Arc from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Arc release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Arc to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Arc.

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

-   **[Microsoft 365 and GitHub connectors](https://www.servicenow.com/docs/access?context=connectors-in-cowork&family=zurich&ft:locale=en-US)**

Connect ServiceNow Arc to Microsoft 365 and GitHub so the agent can work with your mail, calendar, files, and repositories. Administrators control which connector operations the agent can perform through connector scopes.

-   **[Sandboxed execution](https://www.servicenow.com/docs/access?context=cowork-architecture-arc&family=zurich&ft:locale=en-US)**

The agent runs scripts and commands in an isolated virtual machine sandbox on the Mac, with access to the files you share. The sandbox image comes from your connected instance, so updates to it apply the next time you launch, sign in, or switch instances.

-   **[Policy management and governance in ServiceNow Arc](https://www.servicenow.com/docs/access?context=policy-management-cowork&family=zurich&ft:locale=en-US)**

Control what the agent can reach and change with network allowlists, sandbox rules, file type rules, and connector scopes, alongside tool gates and approval patterns. Target each policy to specific users and groups with user criteria. The Default Policy applies to everyone, and clients keep enforcing their last policy if the instance is unreachable. Override the Default Policy by creating a policy with a higher priority. The policy with the lowest priority number wins, and when priorities tie, the most restrictive rule wins. The same resolution applies to tool gates, connector scopes, and capability overrides. Tool gates offer an auto approval option alongside Allow, Deny, and require approval.

-   **[Tiered approvals and Auto Mode](https://www.servicenow.com/docs/access?context=action-approval-flow-cowork&family=zurich&ft:locale=en-US)**

Assign each approval pattern a hard gate or a soft gate. Hard asks for approval every time, with **Allow**, and **Deny** options. Soft gates add an **Always allow** option that persists across sessions. Users can review and revoke these grants from the **Approvals** list in Settings.

To reduce prompts, administrators turn on the Auto Approval capability \(**auto\_approval**, off by default\), an AI classifier evaluates soft gate and unmatched tool calls against the user's goal and either proceeds or asks for approval. Hard gates never auto-approve. If the classifier is unavailable, soft gate and unmatched calls proceed, and every classifier and fallback decision is logged.

-   **[Priority-based policy resolution](https://www.servicenow.com/docs/access?context=policy-stacking-precedence-cowork&family=zurich&ft:locale=en-US)**

Override the default policy by creating a policy with a lower priority number. The lowest priority number wins. When priorities tie, the approval pattern with the more specific match wins, and then the more restrictive rule. The same resolution applies to all policy components, including tool gates, connector scopes, and capability overrides. Tool gates offer Allow, Deny, HITL, and Auto.

-   **[Approval pattern Match Mode](https://www.servicenow.com/docs/access?context=action-approval-flow-cowork&family=zurich&ft:locale=en-US)**

Define how an approval pattern matches commands with a single Match Mode field: **Exact**, **Relaxed**, or **Keyword**. Keyword mode requires a tool filter and matches whole words only. Write verbs for the bash tool live in a Keyword approval pattern instead of the bash tool gate. Commands that read credential paths or set sensitive environment variables require approval.

-   **[Skills catalog and slash commands](https://www.servicenow.com/docs/access?context=extending-cowork&family=zurich&ft:locale=en-US)**

Browse skills by source \(Default or Custom\), invocation \(agent invoked or user invoked\), and connector, and see whether each skill's required connector is connected. User invoked skill has a unique slash command; typing it in the composer expands the skill's instructions before you send.

Create custom skills by adding a folder with a SKILL.md file, or let the agent create them from a conversation. When a skill script fails, the agent diagnoses and detects the error, applies a correction to fix it, and retries.

-   **[Bundled skills](https://www.servicenow.com/docs/access?context=extending-cowork&family=zurich&ft:locale=en-US)**

ServiceNow Arc ships with a focused set of default skills, including separate skills for ServiceNow, Microsoft 365, planning and meeting skills.

-   **[Usage Insights analytics](https://www.servicenow.com/docs/access?context=cowork-trace-evaluation&family=zurich&ft:locale=en-US)**

View ServiceNow Arc as an application in Usage Insights, with active users, monthly and daily active users, and sessions. Report on conversations by how they start, success and error rates, user interventions, and the model used, along with connector, MCP, and policy block events.

Build funnels, cohorts, and retention reports, and drill down from aggregate charts to individual users and tasks. Data is scoped to your instance only, and user IDs are hashed.

-   **[Observability in AI Control Tower](https://www.servicenow.com/docs/access?context=cowork-trace-evaluation&family=zurich&ft:locale=en-US)**

Register ServiceNow Arc as a managed AI system in AI Control Tower to monitor its use across your organization. Sessions and traces flow into AI Control Tower, where each trace receives quality, safety, and risk assessment scores. You can drill down from a session to its individual steps, including tool calls and policy decisions.

-   **[Kill switch and heartbeat monitoring in AI Control Tower](https://www.servicenow.com/docs/access?context=cowork-architecture-arc&family=zurich&ft:locale=en-US)**

Monitor and control ServiceNow Arc across your organization from AI Control Tower. The fleet view shows who installs ServiceNow Arc and who is active. Heartbeat monitoring checks each installation at regular intervals and flags any that stop responding, so you can find offline installations before they affect users. If an agent takes unsafe actions, use the kill switch to stop them from escalating. The kill switch revokes credentials and terminates running actions.

-   **[Predictable retry behavior](https://www.servicenow.com/docs/access?context=set-agent-limits-safeguards&family=zurich&ft:locale=en-US)**

The agent stops and reports the problem after a bounded number of attempts on the same task, instead of retrying indefinitely or working around a policy block. When a policy blocks an action, the agent reports the block and the reason and makes no further attempts.

-   **[Automatic app updates](https://www.servicenow.com/docs/access?context=update-cowork&family=zurich&ft:locale=en-US)**

The app checks for updates at start-up, during onboarding, every 30 minutes, and on demand from Settings. A required update shows an Update and Restart screen; updates found in the background appear as a dismissible notification. Each update is signature verified before it installs.

-   **[Model choice across](https://www.servicenow.com/docs/access?context=select-model-folders&family=zurich&ft:locale=en-US)Anthropic Claude, GPT, and Google Gemini**

Choose a model from Anthropic Claude \(Opus 4.6, 4.7, 4.8, and Sonnet 4.6\), OpenAI GPT \(5.4 and 5.5\), and Google Gemini \(3.5 Flash\), all routed through Generative AI Controller. After you connect, the model list comes from the models configured on your instance. Opus 4.8 is the default.

-   **Assist metering and entitlements**

User initiated requests consumes assists, recorded in the generative AI log under the feature name ServiceNow Arc Execution. Check your entitlements to determine whether you have access to ServiceNow Arc.


 -   **[Windows support](https://www.servicenow.com/docs/access?context=install-arc-windows&family=zurich&ft:locale=en-US)**

ServiceNow Arc now supports Windows. On Windows desktop, the Arc application acts as an AI agent that plans and runs multi-step tasks across your enterprise applications, within the governance and security policies your administrators define.

-   **[MCP servers managed by administrators](https://www.servicenow.com/docs/access?context=add-mcp-server-arc&family=zurich&ft:locale=en-US)**

MCP server connectors that administrators configure on the instance appear in ServiceNow Arc ready to connect, so users don't enter a server URL or client ID.

When an administrator deactivates a connector, Arc ends any active session, blocks reconnection, and tells the user why. After the connector is reactivated, users reconnect it themselves.

-   **[Notifications for approvals and reminders](https://www.servicenow.com/docs/access?context=notifications-arc&family=zurich&ft:locale=en-US)**

ServiceNow Arc notifies users about pending approvals and reminders, with one notification for each pending approval before it times out. When users are in another chat, a banner appears at the top of the Arc window. When they're in another app, a desktop notification appears. Users can approve or reject the action from either one.

For more information, see [Turn notifications on or off](https://www.servicenow.com/docs/access?context=manage-notification-settings&family=zurich&ft:locale=en-US).

-   **[Fluent app development for MacOs](https://www.servicenow.com/docs/access?context=app-development-arc&family=zurich&ft:locale=en-US)**

Build, deploy, and edit ServiceNow scoped applications from a conversation in ServiceNow Arc, using the Now SDK, which is preinstalled in the sandbox. The agent presents a build plan for approval, then creates a TypeScript project and authors the data model, server and client logic, flows, UI, AI agents, and tests.

App development isn't supported on Windows.

-   **[File preview](https://www.servicenow.com/docs/access?context=preview-files-arc&family=zurich&ft:locale=en-US)**

Users can preview Word, Excel, PowerPoint, PDF, and PNG files in ServiceNow Arc. From the preview, they can download a file, open it in its native app or its folder, zoom in or out, and view it full screen.


</td></tr><tr><td>

Australia

</td><td>

-   **[Microsoft 365 and GitHub connectors](https://www.servicenow.com/docs/access?context=connectors-in-cowork&family=australia&ft:locale=en-US)**

Connect ServiceNow Arc to Microsoft 365 and GitHub so the agent can work with your mail, calendar, files, and repositories. Administrators control which connector operations the agent can perform through connector scopes.

-   **[Sandboxed execution](https://www.servicenow.com/docs/access?context=cowork-architecture-arc&family=australia&ft:locale=en-US)**

The agent runs scripts and commands in an isolated virtual machine sandbox on the Mac, with access to the files you share. The sandbox image comes from your connected instance, so updates to it apply the next time you launch, sign in, or switch instances.

-   **[Policy management and governance in ServiceNow Arc](https://www.servicenow.com/docs/access?context=policy-management-cowork&family=australia&ft:locale=en-US)**

Control what the agent can reach and change with network allowlists, sandbox rules, file type rules, and connector scopes, alongside tool gates and approval patterns. Target each policy to specific users and groups with user criteria. The Default Policy applies to everyone, and clients keep enforcing their last policy if the instance is unreachable. Override the Default Policy by creating a policy with a higher priority. The policy with the lowest priority number wins, and when priorities tie, the most restrictive rule wins. The same resolution applies to tool gates, connector scopes, and capability overrides. Tool gates offer an auto approval option alongside Allow, Deny, and require approval.

-   **[Tiered approvals and Auto Mode](https://www.servicenow.com/docs/access?context=action-approval-flow-cowork&family=australia&ft:locale=en-US)**

Assign each approval pattern a hard gate or a soft gate. Hard asks for approval every time, with **Allow**, and **Deny** options. Soft gates add an **Always allow** option that persists across sessions. Users can review and revoke these grants from the **Approvals** list in Settings.

To reduce prompts, administrators turn on the Auto Approval capability \(**auto\_approval**, off by default\), an AI classifier evaluates soft gate and unmatched tool calls against the user's goal and either proceeds or asks for approval. Hard gates never auto-approve. If the classifier is unavailable, soft gate and unmatched calls proceed, and every classifier and fallback decision is logged.

-   **[Priority-based policy resolution](https://www.servicenow.com/docs/access?context=policy-stacking-precedence-cowork&family=australia&ft:locale=en-US)**

Override the default policy by creating a policy with a lower priority number. The lowest priority number wins. When priorities tie, the approval pattern with the more specific match wins, and then the more restrictive rule. The same resolution applies to all policy components, including tool gates, connector scopes, and capability overrides. Tool gates offer Allow, Deny, HITL, and Auto.

-   **[Approval pattern Match Mode](https://www.servicenow.com/docs/access?context=action-approval-flow-cowork&family=australia&ft:locale=en-US)**

Define how an approval pattern matches commands with a single Match Mode field: **Exact**, **Relaxed**, or **Keyword**. Keyword mode requires a tool filter and matches whole words only. Write verbs for the bash tool live in a Keyword approval pattern instead of the bash tool gate. Commands that read credential paths or set sensitive environment variables require approval.

-   **[Skills catalog and slash commands](https://www.servicenow.com/docs/access?context=extending-cowork&family=australia&ft:locale=en-US)**

Browse skills by source \(Default or Custom\), invocation \(agent invoked or user invoked\), and connector, and see whether each skill's required connector is connected. User invoked skill has a unique slash command; typing it in the composer expands the skill's instructions before you send.

Create custom skills by adding a folder with a SKILL.md file, or let the agent create them from a conversation. When a skill script fails, the agent diagnoses and detects the error, applies a correction to fix it, and retries.

-   **[Bundled skills](https://www.servicenow.com/docs/access?context=extending-cowork&family=australia&ft:locale=en-US)**

ServiceNow Arc ships with a focused set of default skills, including separate skills for ServiceNow, Microsoft 365, planning and meeting skills.

-   **[Usage Insights analytics](https://www.servicenow.com/docs/access?context=cowork-trace-evaluation&family=australia&ft:locale=en-US)**

View ServiceNow Arc as an application in Usage Insights, with active users, monthly and daily active users, and sessions. Report on conversations by how they start, success and error rates, user interventions, and the model used, along with connector, MCP, and policy block events.

Build funnels, cohorts, and retention reports, and drill down from aggregate charts to individual users and tasks. Data is scoped to your instance only, and user IDs are hashed.

-   **[Observability in AI Control Tower](https://www.servicenow.com/docs/access?context=cowork-trace-evaluation&family=australia&ft:locale=en-US)**

Register ServiceNow Arc as a managed AI system in AI Control Tower to monitor its use across your organization. Sessions and traces flow into AI Control Tower, where each trace receives quality, safety, and risk assessment scores. You can drill down from a session to its individual steps, including tool calls and policy decisions.

-   **[Kill switch and heartbeat monitoring in AI Control Tower](https://www.servicenow.com/docs/access?context=cowork-architecture-arc&family=australia&ft:locale=en-US)**

Monitor and control ServiceNow Arc across your organization from AI Control Tower. The fleet view shows who installs ServiceNow Arc and who is active. Heartbeat monitoring checks each installation at regular intervals and flags any that stop responding, so you can find offline installations before they affect users. If an agent takes unsafe actions, use the kill switch to stop them from escalating. The kill switch revokes credentials and terminates running actions.

-   **[Predictable retry behavior](https://www.servicenow.com/docs/access?context=set-agent-limits-safeguards&family=australia&ft:locale=en-US)**

The agent stops and reports the problem after a bounded number of attempts on the same task, instead of retrying indefinitely or working around a policy block. When a policy blocks an action, the agent reports the block and the reason and makes no further attempts.

-   **[Automatic app updates](https://www.servicenow.com/docs/access?context=update-cowork&family=australia&ft:locale=en-US)**

The app checks for updates at start-up, during onboarding, every 30 minutes, and on demand from Settings. A required update shows an Update and Restart screen; updates found in the background appear as a dismissible notification. Each update is signature verified before it installs.

-   **[Model choice across](https://www.servicenow.com/docs/access?context=select-model-folders&family=australia&ft:locale=en-US)Anthropic Claude, GPT, and Google Gemini**

Choose a model from Anthropic Claude \(Opus 4.6, 4.7, 4.8, and Sonnet 4.6\), OpenAI GPT \(5.4 and 5.5\), and Google Gemini \(3.5 Flash\), all routed through Generative AI Controller. After you connect, the model list comes from the models configured on your instance. Opus 4.8 is the default.

-   **Assist metering and entitlements**

User initiated requests consumes assists, recorded in the generative AI log under the feature name ServiceNow Arc Execution. Check your entitlements to determine whether you have access to ServiceNow Arc.


 -   **[Windows support](https://www.servicenow.com/docs/access?context=install-arc-windows&family=australia&ft:locale=en-US)**

ServiceNow Arc now supports Windows. On Windows desktop, the Arc application acts as an AI agent that plans and runs multi-step tasks across your enterprise applications, within the governance and security policies your administrators define.

-   **[Arc policies in AI Control Tower](https://www.servicenow.com/docs/access?context=manage-arc-policies-aict&family=australia&ft:locale=en-US)**

Administrators author and manage ServiceNow Arc agent policies in AI Control Tower, on the **Arc policies** tab under **Govern** &gt; **Policies**.

-   **[MCP servers managed by administrators](https://www.servicenow.com/docs/access?context=add-mcp-server-arc&family=australia&ft:locale=en-US)**

MCP server connectors that administrators configure on the instance appear in ServiceNow Arc ready to connect, so users don't enter a server URL or client ID.

When an administrator deactivates a connector, Arc ends any active session, blocks reconnection, and tells the user why. After the connector is reactivated, users reconnect it themselves.

-   **[Notifications for approvals and reminders](https://www.servicenow.com/docs/access?context=notifications-arc&family=australia&ft:locale=en-US)**

ServiceNow Arc notifies users about pending approvals and reminders, with one notification for each pending approval before it times out. When users are in another chat, a banner appears at the top of the Arc window. When they're in another app, a desktop notification appears. Users can approve or reject the action from either one.

For more information, see [Turn notifications on or off](https://www.servicenow.com/docs/access?context=manage-notification-settings&family=australia&ft:locale=en-US).

-   **[Fluent app development for MacOs](https://www.servicenow.com/docs/access?context=app-development-arc&family=australia&ft:locale=en-US)**

Build, deploy, and edit ServiceNow scoped applications from a conversation in ServiceNow Arc, using the Now SDK, which is preinstalled in the sandbox. The agent presents a build plan for approval, then creates a TypeScript project and authors the data model, server and client logic, flows, UI, AI agents, and tests.

App development isn't supported on Windows.

-   **[File preview](https://www.servicenow.com/docs/access?context=preview-files-arc&family=australia&ft:locale=en-US)**

Users can preview Word, Excel, PowerPoint, PDF, and PNG files in ServiceNow Arc. From the preview, they can download a file, open it in its native app or its folder, zoom in or out, and view it full screen.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Arc features.

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

-   **[Auto mode for each chat](https://www.servicenow.com/docs/access?context=use-auto-mode-chat&family=zurich&ft:locale=en-US)**

Users choose **Standard** or **Auto** approval for each chat in ServiceNow Arc from the message box, and set a default approval mode in **Settings** &gt; **Approvals** for new chats and background runs, such as scheduled tasks.

To make auto mode available, administrators turn on the Auto Mode capability \(**auto\_approval**\), which is off by default, and set tool gates to **Auto Approval** for the tools that auto mode can cover.

-   **[Microsoft 365 connector permissions](https://www.servicenow.com/docs/access?context=set-m365-permissions&family=zurich&ft:locale=en-US)**

Users set each Microsoft 365 connector capability to **Allow**, **Ask me first**, or **Deny**. With **Ask me first**, an approval card asks the user to allow or deny the action every time it runs, and auto mode never skips it.

Administrators set the upper limit with the **Approval gate** field on each connector scope in a policy. Users can choose only a stricter setting, and capabilities the policy limits show **Set by your organization**. Microsoft 365 scopes turned off on the instance now appear in the list. Existing policies keep their behavior, and the audit log records policy changes and Microsoft 365 write actions.

-   **[Clearer approvals](https://www.servicenow.com/docs/access?context=action-approval-flow-cowork&family=zurich&ft:locale=en-US)**

Approval cards in ServiceNow Arc now name the action and describe what's at stake, such as what the action changes or sends and whether it can be undone. For a command under a hard gate, the card names the command that triggered it.

**Allow always** is renamed **Always Allow**, and standing approvals in **Settings** &gt; **Approvals** describe the whole group of actions they cover.

Accessing a folder outside the workspace asks for approval with a soft gate that offers **Always Allow**, unless an approval pattern in the policy applies a hard gate to that call.

-   **[Schedules management](https://www.servicenow.com/docs/access?context=create-scheduled-tasks&family=zurich&ft:locale=en-US)**

Users create scheduled tasks from **Schedules** in the ServiceNow Arc sidebar or through chat. They can start from a blueprint or a custom reminder, and select **Reminder only** to get a notification instead of running a task.

The list shows every schedule, whether created in chat or in **Schedules**. Users can search the list, run, duplicate, edit, pause, or delete any schedule, and see when it last ran and when it runs next.


</td></tr><tr><td>

Australia

</td><td>

-   **[Auto mode for each chat](https://www.servicenow.com/docs/access?context=use-auto-mode-chat&family=australia&ft:locale=en-US)**

Users choose **Standard** or **Auto** approval for each chat in ServiceNow Arc from the message box, and set a default approval mode in **Settings** &gt; **Approvals** for new chats and background runs, such as scheduled tasks.

To make auto mode available, administrators turn on the Auto Mode capability \(**auto\_approval**\), which is off by default, and set tool gates to **Auto Approval** for the tools that auto mode can cover.

-   **[Microsoft 365 connector permissions](https://www.servicenow.com/docs/access?context=set-m365-permissions&family=australia&ft:locale=en-US)**

Users set each Microsoft 365 connector capability to **Allow**, **Ask me first**, or **Deny**. With **Ask me first**, an approval card asks the user to allow or deny the action every time it runs, and auto mode never skips it.

Administrators set the upper limit with the **Approval gate** field on each connector scope in a policy. Users can choose only a stricter setting, and capabilities the policy limits show **Set by your organization**. Microsoft 365 scopes turned off on the instance now appear in the list. Existing policies keep their behavior, and the audit log records policy changes and Microsoft 365 write actions.

-   **[Clearer approvals](https://www.servicenow.com/docs/access?context=action-approval-flow-cowork&family=australia&ft:locale=en-US)**

Approval cards in ServiceNow Arc now name the action and describe what's at stake, such as what the action changes or sends and whether it can be undone. For a command under a hard gate, the card names the command that triggered it.

**Allow always** is renamed **Always Allow**, and standing approvals in **Settings** &gt; **Approvals** describe the whole group of actions they cover.

Accessing a folder outside the workspace asks for approval with a soft gate that offers **Always Allow**, unless an approval pattern in the policy applies a hard gate to that call.

-   **[Schedules management](https://www.servicenow.com/docs/access?context=create-scheduled-tasks&family=australia&ft:locale=en-US)**

Users create scheduled tasks from **Schedules** in the ServiceNow Arc sidebar or through chat. They can start from a blueprint or a custom reminder, and select **Reminder only** to get a notification instead of running a task.

The list shows every schedule, whether created in chat or in **Schedules**. Users can search the list, run, duplicate, edit, pause, or delete any schedule, and see when it last ran and when it runs next.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Arc features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow Arc features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Arc.

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

Install ServiceNow Arc by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Note:** ServiceNow Arc is available in the ServiceNow Store. For details, see the activation information below.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install ServiceNow Arc by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Note:** ServiceNow Arc is available in the ServiceNow Store. For details, see the activation information below.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Arc we have noted them here.

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

The desktop app runs on macOS computers with Apple silicon or Intel processors, and on Windows computers.


</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

The desktop app runs on macOS computers with Apple silicon or Intel processors, and on Windows computers.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Arc we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Arc, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Arc we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Arc we have noted them here.

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

-   Delegate multistep work to an AI agent on your desktop that works alongside the applications you already use.
-   Control agent autonomy with tiered approval gates, priority based policies, and administrator governance of MCP servers.
-   Choose from Anthropic Claude, OpenAI GPT, and Google Gemini models through Generative AI Controller.
-   Extend the agent with skills, and track adoption and policy activity in Usage Insights.
-   Schedule recurring tasks and reminders from chat or the Schedules view, starting from ready made blueprints.

 See [ServiceNow Arc](https://www.servicenow.com/docs/access?context=servicenow-cowork-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Delegate multistep work to an AI agent on your desktop that works alongside the applications you already use.
-   Control agent autonomy with tiered approval gates, priority based policies, and administrator governance of MCP servers.
-   Choose from Anthropic Claude, OpenAI GPT, and Google Gemini models through Generative AI Controller.
-   Extend the agent with skills, and track adoption and policy activity in Usage Insights.
-   Schedule recurring tasks and reminders from chat or the Schedules view, starting from ready made blueprints.

 See [ServiceNow Arc](https://www.servicenow.com/docs/access?context=servicenow-cowork-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/delta-xanadu-australia/rn-combined-intro.md)

