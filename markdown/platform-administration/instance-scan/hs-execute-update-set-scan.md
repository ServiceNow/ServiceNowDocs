---
title: Execute an update set scan
description: Use an update set scan to run applicable checks against the current versions of records that have updates in the update set. If a record has been modified since it was added to the update set, the scan reflects those later changes. Issues that exist only in the update set version of a record aren't detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/instance-scan/hs-execute-update-set-scan.html
release: yokohama
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 1
breadcrumb: [Execute a point scan, Executing a scan, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Execute an update set scan

Use an update set scan to run applicable checks against the current versions of records that have updates in the update set. If a record has been modified since it was added to the update set, the scan reflects those later changes. Issues that exist only in the update set version of a record aren't detected.

## Before you begin

Role required: admin

## About this task

The scan runs all active checks that apply to the record types in the update set. Applicable checks are determined by matching the tables of the records in your update set against the check definitions in Instance Scan. The following check types run during an update set scan:

-   **Table Check**

    Create a check by selecting **Create a new Table Check** if you know which specific table and conditions you want to test. This check type is applied on only one table at a time. You can also include your own script for more complex capabilities by selecting the **Advanced** option on the form.

-   **Column Type Check**

    Retrieve all records containing a specific column field type from all tables in an instance by selecting **Create a new Column Type Check**. The **Column Type Check** type implements the rule you created to iterate all records matching the target column field type.

-   **Linter Check**

    Create a linter check to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated. You can use the abstract syntax tree to analyze issues with the code.


## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Select the update set from the list.

3.  Select **Scan Update Set** from the **Related Links** list.


## Result

The scan runs applicable checks against the current versions of records that have updates in the update set. To review findings, open the result record and select the Checks related list.

## Example

For example, if your update set contains a business rule, checks that target the business rules table run against that record.

**Parent Topic:**[Execute a point scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/instance-scan/hs-execute-point-scan.md)

