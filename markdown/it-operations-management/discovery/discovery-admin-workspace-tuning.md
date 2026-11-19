---
title: Discovery Admin Workspace Tuning
description: Use the Discovery Admin Workspace Tuning page to scan your instance for configuration issues and review the checks that failed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/discovery-admin-workspace-tuning.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-11-12"
reading_time_minutes: 2
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Tuning

Use the Discovery Admin Workspace Tuning page to scan your instance for configuration issues and review the checks that failed.

To access the Tuning page, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Tuning**.

The Tuning page includes the **Home** and **Checks** tabs.

\[Omitted image "daw-tuning.png"\] Alt text: Discovery Admin Workspace Tuning page

## Tuning checks latest reports

The **Home** tab summarizes the results of the most recent scan of your instance. To view the failed checks behind a chart, select a bar or a donut segment. The **Health Checks** page opens and lists the failed checks for the priority, category, or suite that you selected.

|Report title|Type|Description|
|------------|----|-----------|
|Health score|Indicator|Displays the percentage of active checks that passed in the most recent scan.|
|Checks failed|Indicator|Displays the number of checks that failed in the most recent scan, out of the total number of active checks.|
|Findings|Indicator|Displays the total number of findings from the most recent scan. A failed check can have more than one finding.|
|Failed checks by priority|Bar chart|Displays the number of failed checks for each priority level.|
|Failed checks by category|Donut chart|Displays the number of failed checks for each category, such as Manageability or Performance.|
|Failed checks by suite|Bar chart|Displays the number of failed checks for each suite.|

**Note:** Self monitoring suite checks and their results aren't included in these reports, including the active check totals.

## Tuning check results

View the checks that failed during the last scan, arranged by priority. Each result displays the priority, the number of findings, the check name, the category, the date the check ran, and a description of the issue. Selecting a check name opens a page with more information about the failed check, including the following links:

-   **Show check description**: Displays a description of the issue that the check found.
-   **Documentation on the check**: Displays a link to related documentation, when available.
-   **Check definition page**: Opens the check definition, where you can view the check details, scan findings, and version history.

## Tuning checks

The **Checks** tab lists all configured checks, grouped into the **Discovery suite**, **MID suite**, and **Self monitoring suite** tabs. Each check displays its name, priority, short description, active status, and category. To run a suite manually, select **Run now**. For more information, see [Run Tuning checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/run-tuning-checks.md).

Tuning check suites also run automatically on a schedule. If you don't want a check to run, you can deactivate it. For more information, see [Edit an existing check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/edit-an-existing-check.md).

