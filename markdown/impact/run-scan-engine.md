---
title: Run your first scan with the Scan Engine
description: An initial full Scan Engine completion is required to set a baseline from a series of tasks performed that tune the instance environment to complete future scans quickly and efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/run-scan-engine.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Run your first scan with the Scan Engine

An initial full Scan Engine completion is required to set a baseline from a series of tasks performed that tune the instance environment to complete future scans quickly and efficiently.

## Before you begin

[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-initial-scan-engine-settings.md) before beginning this task.

You can complete the configuration steps directly in the Guided Setup interface or can configure the properties using the indicated navigation path.

Refer to [Full and delta instance scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/scan-engine-parallel-processing.md) for details on the various types of scans that can be executed.

**Important:** Depending on the size of your instance, your first scan could take a few hours to complete. We suggest running your first scan overnight, especially in production instances.

Role required: impact app admin or admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scheduled Scan**.

2.  Select **Execute Now**.

    The scan progress is tracked within Platform Health.

    **Note:** Scan Engine findings are not transmitted to Impact Delivery Instance.

3.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scan Engine** &gt; **Scan Status**.

    See [Track Platform Health trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/scan-engine-diagnostic-dashboards.md):

    -   View the different charts and reports available at **Impact** **Platform Health** **Analytics Dashboard**.
    -   Access refreshed Health Scan Engine dashboards each time a scan is completed.
    The Scan Engine results display with the status of each table that is being scanned.

4.  Integrate with your other environments running Impact and utilize Scan Engine diagnostics.

    You can connect your instances with a one-time configuration, available in both OAuth 2.0 and Basic Auth. Refer to [Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md) for details.

5.  **Mark as Complete** to progress to the next step in Guided Setup.


## What to do next

See [Use automated registration to connect to the Impact Delivery Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/start-automated-registration-IDI.md) to further configure the Impact Store Application and import data from the Impact Delivery Instance.

-   **[Full and delta instance scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/scan-engine-parallel-processing.md)**  
The full and delta instance scan feature enables ServiceNow administrators and developers to initiate, monitor, and manage instance scans directly from the Scan Results list view.
-   **[Initiate and manage scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/initiate-manage-scan-engine.md)**  
Use the Scan Results list view to initiate scans, monitor scan status, and manage scan execution using the Initiate Scan and Force Full Scan buttons.
-   **[Running on-demand scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/using-impact-scan-engine.md)**  
You can initiate some scan types on-demand to run whenever they are required.
-   **[Scan blocking and override behavior scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/understanding-scan-blocking-override-behavior.md)**  
The Scan Engine blocks concurrent scans to protect instance performance. Understanding these rules helps you plan scan execution efficiently and how the system handles concurrent scan requests and when Force Full Scan override is necessary.

**Parent Topic:**[Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Configure update set scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/update-set-scanning-properties.md)

**Next topic:**[Full and delta instance scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/scan-engine-parallel-processing.md)

