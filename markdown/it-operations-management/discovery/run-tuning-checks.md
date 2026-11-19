---
title: Run Tuning checks
description: Run Tuning check suites manually to scan your instance for configuration issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/run-tuning-checks.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 1
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery monitoring and issue resolution, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Run Tuning checks

Run Tuning check suites manually to scan your instance for configuration issues.

## Before you begin

Role required: discovery\_admin or admin

## About this task

The configured checks are listed under the following tabs:

-   Discovery suite
-   MID suite
-   Self monitoring suite

**Note:** The Self monitoring suite creates tasks for the issues it finds instead of tuning recommendations. Its checks and results aren't included in the Tuning **Home** tab reports.

Suites also run automatically on a schedule. To stop a check from running, deactivate it. For more information, see [Edit an existing check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/edit-an-existing-check.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Tuning**.

2.  Select **Checks**.

3.  Select the tab for the suite that you want to run: **Discovery suite**, **MID suite**, or **Self monitoring suite**.

4.  Select **Run now**.

    **Note:** Only one scan can run at a time. Wait for the in-progress scan to finish before you run another suite.


## What to do next

After the scan finishes, review the results on the Tuning **Home** tab. For more information, see [Discovery Admin Workspace Tuning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/discovery-admin-workspace-tuning.md).

