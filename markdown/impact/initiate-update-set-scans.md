---
title: Initiate update set scans
description: Scan open update sets for findings to gain insights into what you're importing and exporting across your environments. When Suite Scan is enabled, choose between scanning all active definitions or a curated suite.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/initiate-update-set-scans.html
release: australia
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 2
keywords: [update set scans, Suite Scan, scan engine]
breadcrumb: [Run on-demand scans, Run your first scan, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Initiate update set scans

Scan open update sets for findings to gain insights into what you're importing and exporting across your environments. When Suite Scan is enabled, choose between scanning all active definitions or a curated suite.

## Before you begin

Local update set scans are performed in batches. Retrieved update set scans are scanned individually.

Role required: scan\_engine\_admin or system administrator

## Procedure

1.  Navigate to **All** &gt; **System Update Sets**, and then select one of the following:

    -   **Local Update Sets**
    -   **Retrieved Update Sets**
2.  Select the name of the update set to scan.

3.  In **Related Links**, select **Update Set Scan**.

4.  Select a scan type.

    -   Full Scan: Scans against all active definitions\[Omitted image "update-set-scan-modal.png"\] Alt text: Full scan modal.
    -   Suite Scan: Scans against a specific suite of definitions. \[Omitted image "update-set-scan-modal-select-scanengine.png"\] Alt text: Suite scan selection modal.

        **Note:** Suite Scan is only available if the **Allow Suite Scan for update sets** property is enabled.

5.  If you selected Suite Scan, select a suite from list.

    -   The Scan Engine suite is one that is provided as an example suite that, once populated with Definitions, can be selected for the suite scan to complete.
    -   If an Update Set completion condition includes a specific suite name value, or that Suite is empty \(requiring a full scan\) and your scan doesn't meet the criteria, an error message is returned with a link to update the settings and repeat your scan.
    \[Omitted image "scan-suite-error.png"\] Alt text: Update set error message when the suite is empty in the configuration.

6.  Review the update set completion enforcement message.

    If update set completion enforcement is enabled, a message appears to indicate what requirements must be met to complete the update set. The message changes based on your scan selection and the configured enforcement condition.

<table><thead><tr><th>

Scan Type Selected

</th><th>

Enforcement Message

</th></tr></thead><tbody><tr><td>

Full Scan

</td><td>

Displays no specific suite requirement. The scan validates against all active definitions to meet the completion condition.

</td></tr><tr><td>

Suite Scan with Scan Engine Selected

</td><td>

Displays: "The Scan Engine 'Update Set completion condition' requires a scan result with the 'Scan Engine' Suite. Choose Suite Scan below and select 'Scan Engine' to satisfy this requirement if your intention is to complete this update set."**Note:** In this example 'Scan Engine' suite is required, but your Scan Engine administrator may have configured any Suite name, or 'Suite is empty' to require a full scan of all update sets.

</td></tr></tbody>
</table>7.  Select **Start Scan** to run the scan.

8.  Review the scan results.

    If the scan fails to meet completion criteria, a message explains which conditions were not met.


**Parent Topic:**[Run on-demand scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/using-impact-scan-engine.md)

**Related topics**  


[Configure update set scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/update-set-scanning-properties2.md)

[Customize Scan Engine definition suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definition-suites.md)

