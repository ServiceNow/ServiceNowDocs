---
title: Execute a point scan
description: Execute all applicable checks against a single record, update set or an application by selecting Run Point Scan.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Executing a scan, Use, Instance Scan, Maintain and monitor, Administer]
---

# Execute a point scan

Execute all applicable checks against a single record, update set or an application by selecting **Run Point Scan**.

## Before you begin

Role required: admin

## About this task

For example, if you execute a point scan against a business rule, only the checks that are applicable to the business rule table run, and only that single target record is scanned. If an update set scan or an application scan is executed, all records related to that update set or application are scanned.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

2.  Navigate to the record in a table applicable for point scan.

    **Note:** The **Run Point Scan** related link appears in the UI only for applicable records.

3.  Scroll down to the **Related Links** section.

4.  Select the **Run Point Scan** related links.

    **Note:** The **Run Point Scan** related link is available only if all the following conditions are true.

    -   Available checks that are applicable to the record
    -   The record is active
    -   The user has read access to the record
    -   The record is on a table that extends sys\_metadata
    -   The role of the user must be scan\_user
    -   The system property **glide.scan.enable\_point\_scan\_ui\_action** must not be false
    The progress tracker appears showing the status of the scan.

5.  Select **Go to Result**.

    The Scan Result record appears.

6.  Select **Checks** related list to look at the findings.

    If you want to review the failure reasons, select the **Failures** related list.


## Result

A scan of all applicable checks against only a single record is executed.

-   **[Execute an update set scan](hs-execute-update-set-scan.md)**  
Use update set scan to execute applicable checks against records that are affected by the update set.
-   **[Execute an app scan](hs-execute-app-scan.md)**  
Scan the installed files of an application as well as the application record itself with applicable checks by executing an application scan.

**Parent Topic:**[Executing a scan](../reference/hs-execute-scans.md)

**Related topics**  


[Execute a test scan](hs-execute-test-scan.md)

[Execute a full scan](hs-execute-full-scan.md)

[Execute a suite scan](hc-execute-suite-scan.md)

[Execute a reactive scan](hs-reactive-scan.md)

