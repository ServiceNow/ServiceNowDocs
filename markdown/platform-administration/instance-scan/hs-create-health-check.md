---
title: Create a check
description: Create your own checks by implementing the following procedure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/instance-scan/hs-create-health-check.html
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Create a check

Create your own checks by implementing the following procedure.

## Before you begin

Role required: scan\_admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

2.  Select **New** from the Checks context menu.

    The Check Interceptor list appears.

3.  Select one of the available types of checks.

    See [Check types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-intro-health-check.md) for more information.

    **Note:** If you want to update an existing check, the **Version** field increments itself. The new version provides you a change history. You can also know which particular version of the check ran with a given scan.


-   **[Create a table type check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-create-table-health-check.md)**  
Create a check by selecting **Create a new Table Check** if you know which specific table and conditions you want to test. This check type is applied on only one table at a time. You can also include your own script for more complex capabilities by selecting the **Advanced** option on the form.
-   **[Create a column type check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-create-column-health-check.md)**  
Retrieve all records containing a specific column field type from all tables in an instance by selecting **Create a new Column Type Check**. The **Column Type Check** type implements the rule you created to iterate all records matching the target column field type.
-   **[Create a script only check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-create-script-health-check.md)**  
Create a check without specifying a table or a column type by selecting **Create a new Script Only Check**. You can verify meta data, configurations, and execute complex checks by writing your own script.
-   **[Create a linter check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hc-linter-check.md)**  
Create a linter check to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated. You can use the abstract syntax tree to analyze issues with the code.

**Parent Topic:**[Using Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-using-scans.md)

**Related topics**  


[Create a check suite]()

[Executing a scan]()

[Schedule a full scan]()

[Schedule a suite scan]()

[Monitoring a scan]()

[Parallel scans]()

[Reviewing of scans]()

[Queue your scan]()

[Cancel a scan]()

[Using the Instance Scan dashboard]()

