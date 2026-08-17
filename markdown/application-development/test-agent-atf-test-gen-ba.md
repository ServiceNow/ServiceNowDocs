---
title: ATF test generation in Build Agent
description: The Build Agent can generate Automated Test Framework \(ATF\) tests while you create or edit applications. This capability helps validate your builds with consistent, automated test coverage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/test-agent-atf-test-gen-ba.html
release: australia
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Use, Test Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# ATF test generation in Build Agent

The Build Agent can generate Automated Test Framework \(ATF\) tests while you create or edit applications. This capability helps validate your builds with consistent, automated test coverage.

## Key benefits

ATF test generation in Build Agent provides these benefits:

-   Automated test creation during application development reduces manual test authoring effort
-   AI-driven test generation ensures consistent test patterns and improved coverage
-   Failed tests are automatically triaged to help you quickly identify and address issues
-   User consent gates ensure applications only generate tests when explicitly authorized

## How it works

The following information describes how ATF test generation integrates with the Build Agent workflow:

-   After successfully building and installing an application, the Build Agent displays a consent prompt asking whether you want to generate automated tests for the application
-   If you accept, the Build Agent generates test cases using ATF patterns and best practices
-   Generated tests run through quality validators to ensure consistency and coverage
-   You can opt out entirely with a feature flag if your team doesn't use automated testing

## User workflow

The ATF test generation workflow follows this sequence:

1.  You create or edit an application using the Build Agent
2.  You complete the build and install process
3.  The Build Agent displays a consent prompt: "Generate automated tests for this application?"
4.  You choose one of the following:
    -   **Yes** — Proceed with test generation
    -   **No** — Skip test generation for this build
    -   **Remind me later** — Defer the decision until the next build
5.  If you select **Yes** and after test generation completes, the Build Agent automatically executes the server-side tests. If the Run UI ATF tests setting is enabled, the client-side UI tests run automatically as well. You can also manually trigger UI tests at any time.

