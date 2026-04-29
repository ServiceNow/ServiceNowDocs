---
title: Scan Engine for the Impact Store Application
description: Impact Platform Health uses the Impact Scan Engine to enable proactive management of instance quality, compliance, and performance. The Scan Engine is integrated with your Impact Store App to support platform health and adherence to leading practices.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Health, Using Impact, Impact]
---

# Scan Engine for the Impact Store Application

Impact Platform Health uses the Impact Scan Engine to enable proactive management of instance quality, compliance, and performance. The Scan Engine is integrated with your Impact Store App to support platform health and adherence to leading practices.

The Scan Engine examines ServiceNow instances for findings related to active definitions that are stored in the Scan Findings table. You can view existing or resolved findings that resulted from the instance scans or summarized and detailed scan information.

Impact Scan Engine automates your code inspections in real-time so you can identify more deficiencies, improve the quality of your instances, and speed up your development efforts. You can also monitor and control development activities to proactively improve the quality of the system and support ongoing efforts to improve it over time.

## Benefits and overview

-   Enforce leading practices and code standards in real-time.
-   Enhance platform performance, security, and user experience with role-based visibility and controls.
-   Improve maintainability, upgrades, and problem management.
-   Reduce development and maintenance costs.
-   Diminish the need for manual code reviews, which are prone to human error.
-   Calculate technical debt and estimate resolution time with scan output findings, progress percentiles, and estimated time remaining on code fixes.
-   Empower proactive code quality monitoring and detection versus reactive corrections.
-   Automate developer feedback and training through real-time, leading practice rule evaluations.

## Scan definitions

Scan Engine uses a large set of definitions to correct coding and workflow findings in real time and performs scans across your entire instance to detect existing findings. This prevents developer mistakes by blocking saving a record before issues are resolved. Nightly scans identify existing findings across the entire instance.

For more information, see [Scan Engine definitions](scan-engine-definitions.md).

## Scan types

There are different types of scans that you can run on your instances. Depending on the type of scan, the properties required during configuration vary.

Refer to the table for information on the available scan types.

<table><thead><tr><th>

Scan type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Initial diagnostic scan \(Scheduled scan\)

</td><td>

-   Runs based on defined Scheduled Scan options or on-demand with the Execute Now option.

**Note:** The first executed instance scan is a full scan.

See [Run your first scan with the Scan Engine](../task/run-scan-engine.md) for first time setup.

-   View existing or resolved findings that resulted from the instance scans as well as summarized and detailed scan information.

</td></tr><tr><td>

Diagnostic scans- On-demand scan \(subsequent delta scans\)

</td><td>

-   Scans for configured updates that occurred since the last scan.
-   Specifically analyzes application files that have been modified or sys\_update\_xml records.
-   Delta scans always look for definitions marked to return one row check per system property.
-   Scans for specific definitions that were identified as development issues in a previous scan.

**Note:** See [Configure Scan Engine properties](../task/configure-scan-engine-properties.md) for on-demand scan configuration options.


</td></tr><tr><td>

Update set scan

</td><td>

-   Scans individual update sets for findings.

The initial Update set scan is a full scan of all open update sets. Subsequent scans only scans records that have been modified since the last scan date \(delta scan\).

-   Child update set findings are visible from the parent update set findings summary scan record.

**Note:** See [Configure update set scanning properties](../task/update-set-scanning-properties.md) for details.


</td></tr><tr><td>

Application scan

</td><td>

Scan applications to identify definition findings before publishing to the application repository. **Note:** See [Initiate application scans](../task/initiating-on-demand-scans-scan-engine.md)for details.

</td></tr></tbody>
</table>## Configuration overview

For more information on configuring and running the Scan Engine, see [Running on-demand scans](../task/using-impact-scan-engine.md), and [Analytics Dashboards](scan-engine-diagnostic-dashboards.md).

**Note:** Scan Engine findings are not transmitted to Impact Delivery Instance through the Guided Setup integration.

