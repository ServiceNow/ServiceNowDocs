---
title: View Early Warning for Security Exposure Management integration health
description: Monitor the Early Warning for Security Exposure Management integration by reviewing run history, ingestion performance, and processing health from the Security Exposure Management Administration console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/view-armis-early-warning-health.html
release: australia
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [Armis Early Warning, integration health, ingestion health, integration runs]
breadcrumb: [Early Warning for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# View Early Warning for Security Exposure Management integration health

Monitor the Early Warning for Security Exposure Management integration by reviewing run history, ingestion performance, and processing health from the Security Exposure Management Administration console.

## Before you begin

The Early Warning for Security Exposure Management integration must be installed and at least one integration run must have completed successfully.

Role required: sn\_vul\_int\_fw.read\_integrations

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **Administration**.

2.  In the **Integrations** list, select **Review** under Early Warning for Security Exposure Management tile.

    The Early Warning for Security Exposure Management Overview page opens, displaying integration health charts and the integrations table.

3.  Review the **Integration runs** chart to confirm that recent runs completed successfully.

    The chart displays the number of runs over the selected time period, color-coded by status. Use the **Since** filter to change the range from the default of last 7 days.

4.  Review the **Ingestion health** chart to check API and queue response times.

    The chart shows three metrics measured in seconds: **REST API time**, **Import queue wait time**, and **Import queue processing time**.

5.  Review the **Processing health** chart to check data processing performance over the last 30 days.

    The chart displays the following metrics: **VI creation time**, **Risk rules time**, **Remediation task rules time**, **CI lookup time**, and **Assignment rules time**.

6.  In the **Integrations** table, check the **Last run status** column for the **Early Warning for Security Exposure Management** row.

    A status of **Success** with the note "Successfully completed integration run. No more data to process at this time." confirms that the integration is current and no new CVEs arrived in the last run.


**Parent Topic:**[Early Warning for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/armis-early-warning-integration.md)

