---
title: Run Scan Engine
description: Run an initial full instance scan to set a baseline to tune the instance environment to complete future scans quickly and efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/run-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Impact Guided Setup, Configuring Impact, Impact]
---

# Run Scan Engine

Run an initial full instance scan to set a baseline to tune the instance environment to complete future scans quickly and efficiently.

## Before you begin

[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-initial-scan-engine-settings.md) before beginning this task.

You can complete the configuration steps directly in the Guided Setup interface or can configure the properties using the indicated navigation path.

Refer to [Monitor and manage instance health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md) for details on the various types of scans that can be executed.

**Important:** Depending on the size of your instance, your first scan could take a few hours to complete. We suggest running your first scan overnight, especially in production instances.

Role required: impact app admin or admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scheduled Scan**.

2.  Select **Execute Now**.

    The scheduled script executions table displays identifying all scripts that run during the scheduled scan.

    **Note:** Scan Engine findings aren't transmitted to Impact Delivery Instance.

3.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Status**to track the scan progress.

    The results display with the status of each table that is being scanned. See [Manage and monitor scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-manage-scan-engine.md) for additional information on scans and scan results.

4.  Integrate with your other environments running Impact and utilize Scan Engine diagnostics.

    You can connect your instances with a one-time configuration, available in both OAuth 2.0 and Basic Auth. Refer to [Configure Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-integration-scan-engine.md) for details.

5.  **Mark as Complete** to progress to the next step in Guided Setup.


## What to do next

See [Use automated registration to IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/start-automated-registration-IDI.md) to further configure the Impact Store Application and import data from the Impact Delivery Instance.

-   **[Run on-demand scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/using-impact-scan-engine.md)**  
You can initiate on-demand scans outside of the already regularly scheduled instance scans.
-   **[Scan Engine Headless REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-headless-api-overview.md)**  
The Scan Engine API gives you a way to trigger scans programmatically, retrieve findings in real-time, and integrate scan automation into your business processes. Rather than running scans from the user interface, call REST endpoints from Continuous Integration/Continuous Deployment \(CI/CD\) pipelines, scheduled jobs, or custom workflows.
-   **[Scan blocking and override behavior scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/understanding-scan-blocking-override-behavior.md)**  
The Scan Engine blocks concurrent scans to protect instance performance. Understanding these rules helps you plan scan execution efficiently, handle concurrent scan requests, and determine when Force Full Scan override is necessary.

**Parent Topic:**[Impact Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/guided-setup-impact-in-app.md)

