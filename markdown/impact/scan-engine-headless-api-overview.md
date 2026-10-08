---
title: Scan Engine Headless REST API
description: The Scan Engine API gives you a way to trigger scans programmatically, retrieve findings in real-time, and integrate scan automation into your business processes. Rather than running scans from the user interface, call REST endpoints from Continuous Integration/Continuous Deployment \(CI/CD\) pipelines, scheduled jobs, or custom workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-headless-api-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-23"
reading_time_minutes: 3
keywords: [Scan Engine, API, headless, automation]
breadcrumb: [Scan your instance, Configuring Impact, Impact]
---

# Scan Engine Headless REST API

The Scan Engine API gives you a way to trigger scans programmatically, retrieve findings in real-time, and integrate scan automation into your business processes. Rather than running scans from the user interface, call REST endpoints from Continuous Integration/Continuous Deployment \(CI/CD\) pipelines, scheduled jobs, or custom workflows.

With Scan Engine API, you can:

-   Automate scans by triggering them from CI/CD pipelines, scheduled jobs, or custom workflows
-   Retrieve findings programmatically and integrate scan results into your tooling
-   Run headless scans in server-side environments without the user interface
-   Monitor scans in real-time by polling scan status and acting on results immediately
-   Cancel scans that are no longer needed
-   Retrieve findings that have been resolved or fixed over time

## When to use the Scan Engine API

Use the Scan Engine API to:

-   Block deployments based on scan findings and integrate into your CI/CD pipeline to catch issues before code moves to production
-   Run nightly health checks on your CMDB or service mapping without manual action
-   Scan multiple applications in parallel as part of a larger automation workflow
-   Collect and report on scan results over time as part of your monitoring strategy

## Before you start

Requirements:

-   A ServiceNow instance with Scan Engine enabled, running Impact Platform v12.0.0 or later
-   A user account with the **sn\_se.scan\_engine\_user** role
-   Valid session token or OAuth credentials for authentication
-   API access enabled on your instance

## How the API works

The Scan Engine API follows a request-response pattern:

<table><thead><tr><th>

Request

</th><th>

Response

</th></tr></thead><tbody><tr><td>

Trigger a scan

</td><td>

-   Send a POST request to start a scan against an instance, update set, application, or content.
-   Returns a unique scan result ID you can use to track progress.

</td></tr><tr><td>

Check status

</td><td>

Poll the status endpoint to see whether the scan is still running or complete. Returns error and warning counts, and an overall health score.

</td></tr><tr><td>

Retrieve findings

</td><td>

Once the scan completes, fetch the findings endpoint to get detailed results about what was found and where.

</td></tr><tr><td>

Act on results

</td><td>

Use the findings in your workflow to fail a CI/CD build, send an alert, or generate a report.

</td></tr><tr><td>

Cancel scan \(optional\)

</td><td>

Cancel before the scan completes if it is no longer needed,

</td></tr><tr><td>

Retrieve resolved findings \(optional\)

</td><td>

Query for findings that have been fixed or resolved over time to track long-term improvements.

</td></tr></tbody>
</table>## Key concepts

-   **Scan result ID**

    A unique identifier returned when you start a scan. Use this ID to check status and retrieve findings. It persists in your instance so you can access scan history.

-   **Scan mode**

    The type of scan you're running, either `instance`, `update_set`, `application`, or `content`. Each mode targets a different scope. Suffixed spellings such as `instance_scan` and `application_scan` are also accepted for backward compatibility. The response always echoes the canonical unsuffixed mode name.

-   **Health score**

    A 0–100 score reflecting the overall health of the scanned target. Lower scores indicate more findings. Use this to set thresholds for automated decisions.

-   **Findings**

    Individual violations discovered during a scan. Each finding includes a severity level, a description of the issue, and the affected record. Use findings to prioritize fixes. For a complete list of fields returned in finding responses, see [Scan Engine API field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/finding-resolved-finding-fields.md).

-   **Trigger channel**

    The declared origin of the scan request, either API, UI, or Scheduled. Use this field to determine whether a scan was triggered programmatically.


-   **[Trigger a scan via API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/trigger-scan-api.md)**  
You can start a Scan Engine scan by sending a POST request to the scan endpoint. The API returns a unique scan result ID that you use to check progress and retrieve findings.
-   **[Check scan status and retrieve findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/check-scan-status-retrieve-findings.md)**  
After triggering a scan, poll the status endpoint to monitor progress and retrieve findings when the scan completes.
-   **[Automate scans in CI/CD pipelines and scheduled workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/integrate-scan-engine-ci-cd.md)**  
Use the Scan Engine API to automate scans in Continuous Integration/Continuous Deployment \(CI/CD\) pipelines and scheduled jobs, enabling you to block risky changes or monitor instance health programmatically.

**Parent Topic:**[Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md)

