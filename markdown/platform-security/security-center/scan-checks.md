---
title: Scan checks
description: Use checks to detect anomalies within an instance, running against tables, records, or metadata.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security scanner, Security configuration console, Security Center, Platform Security]
---

# Scan checks

Use checks to detect anomalies within an instance, running against tables, records, or metadata.

![SC Auditor suite findings](../images/sec-center-checks.png)

Checks are rules designed to detect anomalies within an instance. Select a check on the list to view details including what the check evaluates, and possible steps to correct the issue if the check returns any findings.

Select the **+Create task** button to create a Security Task related to a scan check. For details on Security Tasks, see [Security Tasks](security-task-manager.md).

Checks are divided into four classes to identify issues and implement security recommendations for your organization: table checks, column type checks, script only checks, and linter checks.

|Check class|Description|
|-----------|-----------|
|Table checks|Use this check class when you know the specific tables and checks you want to test.|
|Column checks|Use this check class to implement the rule you created to iterate all records matching the target column field type.|
|Script checks|Use this check class to verify meta data, configurations, and execute complex checks by writing your own checks.|
|Linter checks|Use this check class to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated which can be used to analyze issues with the code.|

**Parent Topic:**[Security scanner](sc-scanning.md)

