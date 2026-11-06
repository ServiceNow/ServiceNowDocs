---
title: Run Scan Engine
description: Run an initial full instance scan to set a baseline to tune the instance environment to complete future scans quickly and efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/run-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Platform Health, Using Impact, Impact]
---

# Run Scan Engine

Run an initial full instance scan to set a baseline to tune the instance environment to complete future scans quickly and efficiently.

## Before you begin

[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-initial-scan-engine-settings.md) before beginning this task.

You can complete the configuration steps directly in the Guided Setup interface or can configure the properties using the indicated navigation path.

**Important:**

-   Refer to [Full and delta scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/scan-engine-parallel-processing.md) for details on the various types of scans that can be executed.
-   Depending on the size of your instance, your first scan could take a few hours to complete. We suggest running your first scan overnight, especially in production instances.

Role required: impact app admin or admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scheduled Scan**.

2.  Select **Execute Now**.

    The scheduled script executions table displays identifying all scripts that run during the scheduled scan.

    **Note:** Scan Engine findings aren't transmitted to Impact Delivery Instance.

3.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Status**to track the scan progress.

    The results display with the status of each table that is being scanned. See [Initiate and monitor scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/initiate-manage-scan-engine.md) for additional information on scans and scan results.

4.  Integrate with your other environments running Impact and use Scan Engine diagnostics.

    You can connect your instances with a one-time configuration, available in both OAuth 2.0 and Basic Auth. Refer to [Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md) for details.

5.  **Mark as Complete** to progress to the next step in Guided Setup.


