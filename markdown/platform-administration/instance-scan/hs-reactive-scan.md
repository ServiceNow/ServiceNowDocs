---
title: Execute a reactive scan
description: Execute a reactive scan to set up a scan that runs automatically on an execution tracker failure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/instance-scan/hs-reactive-scan.html
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Executing a scan, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Execute a reactive scan

Execute a reactive scan to set up a scan that runs automatically on an execution tracker failure.

## Before you begin

Role required: admin.

## About this task

For many failed processes on your instance, you can find a corresponding record on the execution tracker. The progress window shows the status of the test. If a process fails on an execution tracker, Instance Scan can watch for that failure on the progress status and run a scan automatically.

The **Trigger Type** in the Scan Trigger form should match the **Source Table** field on the sys\_execution\_tracker record of the failed process to enable the connection between the two. For example, if the failed test is in the Update Sets list, you can set up the **Trigger Type** as sys\_update\_set. This enables Instance Scan to be connected to the execution tracker test failure.

## Procedure

1.  Enter `scan_trigger_list.do` in the navigation filter.

    A list of scan triggers shows up.

2.  Select the required trigger from the list to update it.

    **Note:** The **Trigger Type** is based off of table names. You can also create a custom trigger type in your codes.

    \[Omitted image "hs-trigger-type.png"\] Alt text: Image showing the Scan Trigger form

    The reactive scan is now set up to automatically scan the execution tracker of the failed process which appears on the scan results table.


**Parent Topic:**[Executing a scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-execute-scans.md)

**Related topics**  


[Execute a point scan]()

[Execute a test scan]()

[Execute a full scan]()

[Execute a suite scan]()

