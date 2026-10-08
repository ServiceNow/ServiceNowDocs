---
title: Execute a scan suite as a provider
description: Execute a scan suite to identify issues in your instance and review the scan results.Modify the scan suite schedule to change when a scan suite runs automatically in your instance.Edit, run a test scan on, or rescan an individual scan check from the Scan suites tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-execute-scan-check.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [scan check, edit scan check, test scan, rescan]
breadcrumb: [Use for providers, Service Exchange for Providers, Service Exchange]
---

# Execute a scan suite as a provider

Execute a scan suite to identify issues in your instance and review the scan results.

## Before you begin

Role required: admin \(sb\_admin\)

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Provider Center**.

2.  Select the **Scan suite** tab.

3.  Select one or more scan suites to execute.

    You can select multiple scan suites based on your requirements. Use the filter builder to filter scan results based on specific criteria.

4.  Select **Execute scan suite**.

    The system runs the selected scan suites and displays the results. If no issues are found, the message "Scan complete with no issues" appears. If issues are found, a banner displays the number of issues.

5.  If issues are found, click Go to issues to view the complete list of issues.

    You see all identified issues categorized by priority: high, medium, and low. You can click an individual issue to view resolution details.


**Parent Topic:**[Using Service Exchange for providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-administer.md)

## Modify the scan suite schedule as a provider

Modify the scan suite schedule to change when a scan suite runs automatically in your instance.

### Before you begin

Role required: admin \(sb\_admin\)

### Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Provider Center**.

2.  From the **Scan suite** tab, select the scan suite you want to modify.

3.  Select **Modify Schedule**.

4.  Update the schedule timing as needed, and select **Modify**.


**Related topics**  


[Service Exchange Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-se-center.md)

## Manage a scan check as a provider

Edit, run a test scan on, or rescan an individual scan check from the **Scan suites** tab.

### Before you begin

Role required: admin \(sb\_admin\)

### Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Provider Center**.

2.  Select the **Scan suite** tab.

3.  Select a scan suite, then select the scan check you want to manage.

    You can filter the scan check list by scan suite.

4.  From the scan check panel, select one of the following actions.

    |Action|Description|
    |------|-----------|
    |**Edit**|Modify the scan check's configuration.|
    |**Test scan**|Run this individual check on demand, without executing the full scan suite.|
    |**Rescan**|Re-validate a previously flagged check from the scan check results page.|


**Related topics**  


[Service Exchange Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-se-center.md)

[se-scan-check-details]

[Execute a scan suite as a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-execute-scan-check.md)

