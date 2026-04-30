---
title: Resolving Configuration Compliance import issues
description: Resolve issues with third-party integration import.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Resolving Configuration Compliance import issues

Resolve issues with third-party integration import.

<table id="table_vks_thr_ns"><thead><tr><th>

Issue

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

Test results are missing

</td><td>

Check the **Start Time** on the **Qualys PC Results** integration. It might not be set back far enough. See [Modify Qualys PC Results start date](../task/modify-test-results-startdate.md).

</td></tr><tr><td>

The integration is failing

</td><td>

Check the **Vulnerability Integration Run** status. Individual integration process entries hold the imported XML, which can be examined for unexpected information.

 Navigate to **Qualys Vulnerability Integration** &gt; **Primary Integrations** &gt; **QualysPC Results** &gt; **Vulnerability Integration Runs** related tab.

 Choose the latest run.

 Examine the status and notes of the entries in the related list **Vulnerabilty Integration Process** for anomalies.

.

</td></tr></tbody>
</table>