---
title: Modify Qualys PC Results start date
description: If data is missing for the start date in the Qualys PC Results import, it can be modified.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Resolving Configuration Compliance import issues, Configuration Compliance reference information, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Modify Qualys PC Results start date

If data is missing for the start date in the Qualys PC Results import, it can be modified.

## Before you begin

Role required: sn\_vul\_qualys.admin

## Procedure

1.  Navigate to **All** &gt; **Qualys Vulnerability Integration** &gt; **Administration** &gt; **Primary Integrations**.

2.  Click **Qualys PC Results** integration.

3.  Click **Integration Details**.

4.  Set the **Start time** field to a value in the past, so all scanned and detected test results, since that time, are detected.

    **Note:** If the date is left empty, no data is returned on the first run. Set the value to a maximum of a month in the past. This setting keeps large amount of data from exceeding the Qualys API rate limitations, as well as triggering execution timeouts.

5.  Click **Submit** or **Update**.

6.  Click **Execute Now** to run immediately.


**Parent Topic:**[Resolving Configuration Compliance import issues](../concept/vuln-config-compl-troubleshooting.md)

