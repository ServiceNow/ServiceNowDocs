---
title: Exploring Instance Scan
description: If you are new to Instance Scan, read this overview to learn what the tool can do. Follow the tutorial to create checks and execute scans that uses most basics of Instance Scan features.
locale: en-US
release: australia
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Exploring Instance Scan

If you are new to Instance Scan, read this overview to learn what the tool can do. Follow the tutorial to create checks and execute scans that uses most basics of Instance Scan features.

**Note:** Instance Scan doesn't fully support domain separation. Findings are visibly domain separated based on the domain of the source record. For more information see [Domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md).

## Instance Scan overview

Instance Scan uses the following records, components and scan types.

-   **Checks**

    Checks are singular focused rules that detect anomalies or opportunities in an instance. These checks can run against tables, records, or metadata. Checks are defined to identify security, upgrade best practices, manageability, user experience and performance vulnerabilities. See [Getting started with checks](hs-intro-health-check.md) for more information.

-   **Results**

    An Instance Scan result reports the status and type of the scan. See [Results](../reference/hs-review-scans.md) for more information.

-   **Findings**

    A finding is a reference to a record that has violated a rule from a check on the instance. See [Findings](../reference/hs-review-scans.md) for more information.

-   **Dashboard**

    The Instance Scan dashboard is a system-wide visual representation of the health of your instance. The dashboard helps you manage and analyze the full scan results against your instance. See [Instance Scan dashboard](hs-dashboard.md) for more information.

-   **Quota rule**

    A quota rule determines the execution threshold of a scan. The quota rule prevents the instance from running long scans. For example, any scan running longer than the threshold set by the quota rule will result in a failure. See [Quota rules](hs-quota-rules.md) for more information.

-   **Full scan**

    Execute a scan for the entire instance by selecting **Execute Full Scan**. Implementing a full scan runs all the active checks present in your instance.

-   **Point scan**

    Execute all applicable checks against a single record, update set, or an application by selecting **Run Point Scan**. For example, if you execute a point scan against a business rule, only the checks that are applicable to the business rule table run, and only that single target record is scanned. If you execute an update set scan or an application scan, all records related to that update set or application are scanned. See [Execute an app scan](../task/hs-execute-app-scan.md) and [Execute an update set scan](../task/hs-execute-update-set-scan.md) for more information.

-   **Test scan**

    Execute a test scan to verify if the check works as expected. The test scan enables you to test a single check instead of a full scan by selecting a single check and selecting **Test Check** on the Check form.


## Instance Scan users

Instance Scan has the following roles.

|Users|Description|
|-----|-----------|
|scan\_user|The scan\_user role can run different types of scans, read checks, execute checks, and view the findings and results.|
|scan\_check\_writer|This role includes the scan\_user role and provides permission to create new checks.|

## Instance Scan benefits

<table id="table_c3z_nm2_bbc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Create checks and check suites to know the health of your instance

</td><td>

-   [Getting started with checks](hs-intro-health-check.md)
-   [Create a check](../task/hs-create-health-check.md)
-   [Create a check suite](../task/hc-create-check-suite.md)

</td><td>

scan\_user

</td></tr><tr><td>

Execute scans on the created checks to review the instance health

</td><td>

[Executing a scan](../reference/hs-execute-scans.md)

</td><td>

scan\_user

</td></tr><tr><td>

Scheduling of scans and suite scan

</td><td>

-   [Schedule a full scan](../task/hs-schedule-full-scan.md)
-   [Schedule a suite scan](../task/hc-schedule-suite-scan.md)

</td><td>

scan\_user

</td></tr><tr><td>

Monitor your scans to ensure no health issues of your instance

</td><td>

[Monitoring a scan](../task/hs-progress-status-full-scan.md)

</td><td>

scan\_user

</td></tr><tr><td>

Manage and analyze the results of full scan against your instance

</td><td>

[Instance Scan dashboard](hs-dashboard.md)

</td><td>

scan\_user

</td></tr></tbody>
</table>## What to explore next

To learn more about using Instance Scan, see:

-   [Configuring Instance Scan](hs-intro-scans.md)
-   [Using Instance Scan](hs-using-scans.md)
-   [Instance Scan references](../reference/hs-references.md)

