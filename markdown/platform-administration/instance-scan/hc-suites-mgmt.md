---
title: Suites management
description: A suite is a collection of individual checks and suites that can be used for a scan. Suites can be created for specific business needs. All child suites are executed when a parent suite is used in a scan.
locale: en-US
release: yokohama
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Suites management

A suite is a collection of individual checks and suites that can be used for a scan. Suites can be created for specific business needs. All child suites are executed when a parent suite is used in a scan.

Navigate to **Instance Scan** &gt; **Suites**. Select one of the suites from the list. Select **Execute Suite Scan** to run a suite scan. See [Execute a suite scan](../task/hc-execute-suite-scan.md) for more information.![Image showing a suite](../image/hc-suites.png)

**Note:** Some ServiceNow provided suites are protected suites and the checks in the suite are not modifiable. For example, if you have a suite from the app store, the suite is unmodifiable. You can't add a child suite to the unmodifiable suite. But you can add a parent suite because it doesn't affect the suite.

