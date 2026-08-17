---
title: Enable ATF test generation in Build Agent
description: Enable the Build Agent to generate Automated Test Framework \(ATF\) tests automatically when you build and install applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/test-agent-enable-atf-test-gen-ba.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [ATF test generation in Build Agent, Use, Test Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Enable ATF test generation in Build Agent

Enable the Build Agent to generate Automated Test Framework \(ATF\) tests automatically when you build and install applications.

## Before you begin

-   The Automated Test Framework \(ATF\) plugin is installed and activated on your instance
-   The Build Agent is configured and available in your development environment

Role required: admin

## About this task

When ATF test generation is enabled or have auto-approve setting turned on, the Build Agent automatically offers to create automated tests each time you build and install an application. This reduces manual testing effort and verifies consistent test coverage.

## Procedure

1.  In the IDE, open the ServiceNow Otto panel on the right side and navigate to **Settings** &gt; **General**.

2.  Verify the Build Agent settings for ATF test generation:

    Both settings are disabled by default. Review the following settings in Build Agent:

    |Setting|Default|Purpose|
    |-------|-------|-------|
    |**Sync ATF tests with app**|Disabled|Generates ATF tests when Build Agent creates an app, and keeps them synced when the app is edited.|
    |**Run UI ATF tests**|Disabled|Runs the client-side UI ATF tests and the server-side tests. Requires **Sync ATF tests with app** to be enabled. UI test runs are slower.|

3.  To enable ATF test generation, set **Sync ATF tests with app** to enabled.

    -   **Enabled:** Build Agent generates ATF tests when you create or edit applications.
    -   **Disabled \(default\):** ATF test generation is turned off.
4.  To run client-side UI ATF tests, set **Run UI ATF tests** to enabled.

    -   **Enabled:** Build Agent runs both server-side and client-side UI ATF tests. UI test runs are slower.
    -   **Disabled \(default\):** Only server-side tests are run.
    **Note:** This setting requires **Sync ATF tests with app** to be enabled.

5.  Save your settings.

6.  Test the configuration by creating or editing an application in the Build Agent.

    -   Complete the build process
    -   After installation, verify that the consent prompt appears: "Generate automated tests for this application?"
    -   Select **Yes, proceed** to confirm your setting is enabled

## Result

After you complete these steps, ATF test generation is enabled in Build Agent. The next time you build and install an application, you will receive a consent prompt asking whether to generate automated tests. The Build Agent creates tests based on your application structure and the configured feature flags.

