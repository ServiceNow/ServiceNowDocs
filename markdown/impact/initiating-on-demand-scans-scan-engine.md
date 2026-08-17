---
title: Initiate application scans
description: Scan applications to identify definition findings before publishing to the application repository. Application scans give insight into health scores, the number of findings, and the total impact of findings within your custom applications. When Suite Scan is enabled, choose between scanning all active definitions or a curated suite.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/initiating-on-demand-scans-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [application scans, Suite Scan, scan engine, Team Dev]
breadcrumb: [Run on-demand scans, Run your first scan, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Initiate application scans

Scan applications to identify definition findings before publishing to the application repository. Application scans give insight into health scores, the number of findings, and the total impact of findings within your custom applications. When Suite Scan is enabled, choose between scanning all active definitions or a curated suite.

## Before you begin

Suite Scan for applications is only available if your Scan Engine Administrator has enabled the **Allow Suite Scan for applications** property.

Role required: scan\_engine\_admin or system administrator

## Procedure

1.  In the navigator, enter `sys_app.list`, and then press `Enter` to open the Custom Applications table.

2.  Select the record of the application you want to scan.

3.  Select **Scan This Application**.

4.  Select a scan type.

    -   Full Scan: Scans against all active definitions.
    -   Suite Scan: Scans against a specific suite of definitions. This option appears only if enabled.
5.  If you selected Suite Scan, select a suite from the list.

    If Team Dev push approval enforcement is enabled, you may see an informational message if the selected suite does not align with your approval criteria.

6.  Select **Proceed** to run the scan.

7.  Review the scan results.

    If the scan fails to meet Team Dev approval criteria, a message explains what requirement was not met.


## Result

View application health scores in the Application Health dashboard by navigating to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Application Health**. Health scores are calculated based on finding severity, count, and policy impact.

**Parent Topic:**[Run on-demand scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/using-impact-scan-engine.md)

**Related topics**  


[Configure application scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-application-scanning-properties.md)

[Customize Scan Engine definition suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definition-suites.md)

