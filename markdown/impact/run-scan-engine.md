---
title: Run Scan Engine
description: Run an initial full instance scan to set a baseline to tune the instance environment to complete future scans quickly and efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/run-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring Impact, Impact]
---

# Run Scan Engine

Run an initial full instance scan to set a baseline to tune the instance environment to complete future scans quickly and efficiently.

## Before you begin

[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-initial-scan-engine-settings.md) before beginning this task.

You can complete the configuration steps directly in the Guided Setup interface or can configure the properties using the indicated navigation path.

**Important:**

-   Refer to [Full and delta scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md) for details on the various types of scans that can be executed.
-   Depending on the size of your instance, your first scan could take a few hours to complete. We suggest running your first scan overnight, especially in production instances.

Role required: impact app admin or admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scheduled Scan**.

2.  Select **Execute Now**.

    The scheduled script executions table displays identifying all scripts that run during the scheduled scan.

    **Note:** Scan Engine findings aren't transmitted to Impact Delivery Instance.

3.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Status**to track the scan progress.

    The results display with the status of each table that is being scanned. See [Initiate and monitor scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-manage-scan-engine.md) for additional information on scans and scan results.

4.  Integrate with your other environments running Impact and utilize Scan Engine diagnostics.

    You can connect your instances with a one-time configuration, available in both OAuth 2.0 and Basic Auth. Refer to [Configure Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-integration-scan-engine.md) for details.

5.  **Mark as Complete** to progress to the next step in Guided Setup.


## What to do next

See [Use automated registration to IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/start-automated-registration-IDI.md) to further configure the Impact Store Application and import data from the Impact Delivery Instance.

-   **[Full and delta scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md)**  
The full and delta instance scan feature with Impact Platform Health Scan Engine enables ServiceNow administrators and developers to initiate, monitor, and manage instance health.
-   **[On-demand scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/using-impact-scan-engine.md)**  
On-demand scans run outside of the already regularly scheduled instance scans.
-   **[Initiate and monitor scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-manage-scan-engine.md)**  
Initiate scans, monitor scan status, and manage scan execution using the Initiate Scan and Force Full Scan buttons.
-   **[Scan Engine Headless REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-headless-api-overview.md)**  
The Scan Engine API gives you a way to trigger scans programmatically, retrieve findings in real-time, and integrate scan automation into your business processes. Rather than running scans from the user interface, call REST endpoints from Continuous Integration/Continuous Deployment \(CI/CD\) pipelines, scheduled jobs, or custom workflows.
-   **[Scan blocking and override behavior scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/understanding-scan-blocking-override-behavior.md)**  
The Scan Engine blocks concurrent scans to protect instance performance. Understanding these rules helps you plan scan execution efficiently, handle concurrent scan requests, and determine when Force Full Scan override is necessary.

**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-other-integration-options.md)

**Next topic:**[Full and delta scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md)

