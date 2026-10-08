---
title: Combined ServiceNow Cowork release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for ServiceNow Cowork from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-servicenowcowork-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Cowork release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for ServiceNow Cowork from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Cowork release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Cowork to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for ServiceNow Cowork.

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

-   **[Microsoft 365 and GitHub connectors](https://www.servicenow.com/docs/access?context=connectors-in-cowork&family=zurich&ft:locale=en-US)**

Connect ServiceNow Cowork to Microsoft 365 and GitHub so the agent can work with your mail, calendar, files, and repositories. Administrators control which connector operations the agent can perform through connector scopes.

-   **[Sandboxed execution](https://www.servicenow.com/docs/access?context=cowork-architecture&family=zurich&ft:locale=en-US)**

The agent runs scripts and commands in an isolated virtual machine sandbox on the Mac, with access to the files you share. The sandbox image comes from your connected instance, so updates to it apply the next time you launch, sign in, or switch instances.

-   **[Policy management and governance in ServiceNow Cowork](https://www.servicenow.com/docs/access?context=policy-management-cowork&family=zurich&ft:locale=en-US)**

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

ServiceNow Cowork ships with a focused set of default skills, including separate skills for ServiceNow, Microsoft 365, planning and meeting skills.

-   **[Usage Insights analytics](https://www.servicenow.com/docs/access?context=cowork-trace-evaluation&family=zurich&ft:locale=en-US)**

View ServiceNow Cowork as an application in Usage Insights, with active users, monthly and daily active users, and sessions. Report on conversations by how they start, success and error rates, user interventions, and the model used, along with connector, MCP, and policy block events.

Build funnels, cohorts, and retention reports, and drill down from aggregate charts to individual users and tasks. Data is scoped to your instance only, and user IDs are hashed.

-   **[Observability in AI Control Tower](https://www.servicenow.com/docs/access?context=cowork-trace-evaluation&family=zurich&ft:locale=en-US)**

Register ServiceNow Cowork as a managed AI system in AI Control Tower to monitor its use across your organization. Sessions and traces flow into AI Control Tower, where each trace receives quality, safety, and risk assessment scores. You can drill down from a session to its individual steps, including tool calls and policy decisions.

-   **[Kill switch and heartbeat monitoring in AI Control Tower](https://www.servicenow.com/docs/access?context=cowork-architecture&family=zurich&ft:locale=en-US)**

Monitor and control ServiceNow Cowork across your organization from AI Control Tower. The fleet view shows who installs ServiceNow Cowork and who is active. Heartbeat monitoring checks each installation at regular intervals and flags any that stop responding, so you can find offline installations before they affect users. If an agent takes unsafe actions, use the kill switch to stop them from escalating. The kill switch revokes credentials and terminates running actions.

-   **[Predictable retry behavior](https://www.servicenow.com/docs/access?context=set-agent-limits-safeguards&family=zurich&ft:locale=en-US)**

The agent stops and reports the problem after a bounded number of attempts on the same task, instead of retrying indefinitely or working around a policy block. When a policy blocks an action, the agent reports the block and the reason and makes no further attempts.

-   **[Automatic app updates](https://www.servicenow.com/docs/access?context=update-cowork&family=zurich&ft:locale=en-US)**

The app checks for updates at start-up, during onboarding, every 30 minutes, and on demand from Settings. A required update shows an Update and Restart screen; updates found in the background appear as a dismissible notification. Each update is signature verified before it installs.

-   **[Model choice across](https://www.servicenow.com/docs/access?context=select-model-folders&family=zurich&ft:locale=en-US)Anthropic Claude, GPT, and Google Gemini**

Choose a model from Anthropic Claude \(Opus 4.6, 4.7, 4.8, and Sonnet 4.6\), OpenAI GPT \(5.4 and 5.5\), and Google Gemini \(3.5 Flash\), all routed through Generative AI Controller. After you connect, the model list comes from the models configured on your instance. Opus 4.8 is the default.

-   **Assist metering and entitlements**

User initiated requests consumes assists, recorded in the generative AI log under the feature name ServiceNow Cowork Execution. Check your entitlements to determine whether you have access to ServiceNow Cowork.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing ServiceNow Cowork features.

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some ServiceNow Cowork features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some ServiceNow Cowork features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Cowork.

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

-   **Activation information**

Install ServiceNow Cowork by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Note:** ServiceNow Cowork is available in the ServiceNow Store. For details, see the activation information below.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Cowork we have noted them here.

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

-   **Additional requirements**

The desktop app runs on macOS computers with Apple silicon or Intel processors.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Cowork we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Cowork, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Cowork we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Cowork we have noted them here.

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

-   Delegate multistep work to an AI agent on your desktop that works alongside the applications you already use.
-   Control agent autonomy with tiered approval gates, priority based policies, and administrator governance of MCP servers.
-   Choose from Anthropic Claude, OpenAI GPT, and Google Gemini models through Generative AI Controller.
-   Extend the agent with skills, and track adoption and policy activity in Usage Insights.

 See [ServiceNow Cowork](https://www.servicenow.com/docs/access?context=servicenow-cowork-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

