---
title: Configure auto test prompting and UI tests
description: Configure test settings to enable automatic test prompting and execution of UI tests in Build Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ba-config-testing.html
release: australia
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Configure auto test prompting and UI tests

Configure test settings to enable automatic test prompting and execution of UI tests in Build Agent.

## Before you begin

Role required: admin

## About this task

For more information on UI tests, see [UI Test Script in Automated Test Framework \(ATF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/test-agent-ui-test-script-atf.md).

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio** or **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Select the Settings icon \[Omitted image "ba-settings-icon.png"\] Alt text: in the Build Agent chat panel.

    \[Omitted image "ba-settings-panel-1.png"\] Alt text: Build Agent panel showing greeting message and the Settings button

3.  Enable the toggles for the following settings in the **General** tab as needed.

<table><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sync ATF tests with app

</td><td>

Generates ATF tests when Build Agent creates an app, and keeps them synced when the app is edited.

</td></tr><tr><td>

Run UI ATF tests

</td><td>

Runs the client-side and server-side UI ATF tests. -   The **Sync ATF tests with app** setting must be enabled.
-   This setting is off by default since UI runs are slower.


</td></tr></tbody>
</table>    \[Omitted image "ba-settings-tests.png"\] Alt text: Settings panel General tab showing Enable web search toggled off, and Sync ATF tests with app and Run UI ATF tests toggled on.


## Result

Build Agent runs ATF tests in conversations based on your settings.

**Parent Topic:**[Build Agent configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/configure-build-agent.md)

