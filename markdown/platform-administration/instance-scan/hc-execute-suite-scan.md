---
title: Execute a suite scan
description: Execute suites of available checks against a specific target to have targeted scan results by selecting Execute Suite Scan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/instance-scan/hc-execute-suite-scan.html
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Executing a scan, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Execute a suite scan

Execute suites of available checks against a specific target to have targeted scan results by selecting **Execute Suite Scan**.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Suites**.

    A list of all suites displays.

2.  Select one of the suites from the list.

    The form for the selected suite displays.

3.  Select **Execute Suite Scan**.

    The **Scan Suites Now** modal displays.

4.  Select a target for the scan.

    \[Omitted image "hc-scan-suites-modal.png"\] Alt text: Image showing the Scan Suites Now modal.

    -   **Full Instance**: Scans all the available records in the instance.
    -   **Scoped App**: Scans selected scoped apps. You can select multiple scoped apps.
    -   **Update Set**: Scans multiple update sets.
5.  Select **Execute Scan**.

    **Note:** If a record is inactive, the checks don't generate any findings for that record.


**Parent Topic:**[Executing a scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-execute-scans.md)

**Related topics**  


[Execute a point scan]()

[Execute a test scan]()

[Execute a full scan]()

[Execute a reactive scan]()

