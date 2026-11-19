---
title: Run diagnostics on an Agent Client Collector agent
description: Run automated self-tests on an Agent Client Collector \(ACC\) agent from the ITOM Infra Services Workspace to identify and address agent issues. View agent errors and invoke the relevant remediation steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/itom-visibility/run-acc-agent-diagnostics.html
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 1
keywords: [ACC, agent diagnostics, agent client collector, diagnostic tests, Infra Services Workspace]
breadcrumb: [Use the Agent Client Collector \(ACC\) admin workspace, Use ITOM Infra Services Workspace, ITOM Infra Services Workspace, ITOM Visibility, IT Operations Management]
---

# Run diagnostics on an Agent Client Collector agent

Run automated self-tests on an Agent Client Collector \(ACC\) agent from the ITOM Infra Services Workspace to identify and address agent issues. View agent errors and invoke the relevant remediation steps.

## Before you begin

-   Agent Client Collector Framework version 6.2.0 or higher must be installed.
-   The agent status must be Up to start a diagnostic run.
-   Role required: agent\_client\_collector\_admin

## About this task

Agent diagnostics runs automated self-tests on an ACC agent directly from the agent record. After a run completes, results appear on the **All Results**, **Full Diagnostics**, and **Partial Diagnostics** tabs.

## Procedure

1.  Navigate to **Workspaces** &gt; **ITOM Infra Services Workspace**.

2.  Select **Manage ACC agents** to view the list of ACC agents.

3.  Select an agent on the **Agents** tab to open the agent record.

4.  In the agent feature tree, select **Diagnostic tests**.

    \[Omitted image "diagnostic-tests.png"\] Alt text: Diagnostic tests for an agent

5.  Select **Run full diagnostics**.

    Results populate across the All Results, Full Diagnostics, and Partial Diagnostics tabs after the run completes. Runs can take up to 60 seconds.

    If results don't appear within 60 seconds, the run timed out. Refresh the page and check for any errors.

    If the MID Server associated with the agent is not reachable, diagnostic runs cannot complete. Verify that the MID Server is running before retrying.

6.  Select an individual test to open its detail page.

    The detail page shows the following information:

<table id="table_nwz_nkj_hjc"><thead><tr><th>

Area

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Summary fields

</td><td>

Severity, last result, last run timestamp, and the agent the test ran on.

</td></tr><tr><td>

Result History tab

</td><td>

A chronological list of past runs with status and expandable log output. Log lines can be copied to the clipboard.

</td></tr><tr><td>

Troubleshooting Guide tab

</td><td>

Step-by-step remediation suggestions.Appears only when the test has a known error code with linked guidance.

</td></tr></tbody>
</table>7.  Select **Run this test** to run the single test from the page.

8.  To rerun only the failed tests, select **Rerun failed tests**.

    This button appears only when the run produced failures. Selecting it re-executes only the failed tests and leaves passing tests unchanged.


**Parent Topic:**[Use the Agent Client Collector \(ACC\) admin workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/use-acc-admin-workspace.md)

