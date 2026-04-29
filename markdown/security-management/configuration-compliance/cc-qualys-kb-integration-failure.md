---
title: Qualys Knowledge Base Integration is failing
description: Resolve Qualys Knowledge Base Integration failure by reducing the payload attachment size received from Qualys to the specified limit.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resolving Qualys Vulnerability Integration issues, Qualys, Integrate with other applications, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Qualys Knowledge Base Integration is failing

Resolve Qualys Knowledge Base Integration failure by reducing the payload attachment size received from Qualys to the specified limit.

## Before you begin

Role required: sn\_vul.vulnerability\_admin

## Procedure

1.  Ensure that the payload attachment size is within the specified limit.

    1.  Navigate to **All** &gt; **Qualys Vulnerability Integration** &gt; **Integration Instances**.
    2.  Select the **Integration Instance Parameters** tab.
    3.  Select **max\_delta\_days** and modify the default value to 3.
2.  If the integration still fails, perform the following steps:

    1.  Navigate to **All** &gt; **Qualys Vulnerability Integration** &gt; **Primary Integrations**.

    2.  Select **Qualys Knowledge Base**.

    3.  Select the **Integration Details** tab.

    4.  In the **Start time** field, select the current date to skip the execution of the run for that day.

    5.  Navigate to **All** &gt; **Qualys Vulnerability Integration** &gt; **Integration Instances**.

    6.  Select the **Integration Instance Parameters** tab.

    7.  Select **kb\_backfill\_full\_import** and modify the default value to true.


## Result

Running the Qualys Knowledge Base Backfill integration updates all the third-party entries \(TPEs\) in the system. While the Qualys Host Detection integration creates a placeholder entry, the Qualys Knowledge Base Backfill integration updates it.

