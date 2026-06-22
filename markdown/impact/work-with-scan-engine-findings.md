---
title: Work with Scan Engine findings
description: You can view and work with open findings resulting from scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/work-with-scan-engine-findings.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Resolve technical debt, Diagnose technical debt, Platform Health, Using Impact, Impact]
---

# Work with Scan Engine findings

You can view and work with open findings resulting from scans.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Open Findings**.

2.  Open the record you want to work with by selecting its **Short Description**.

    The finding record displays the following fields.

    |Field|Description|
    |-----|-----------|
    |**Definition**|Displays the scan definition that detected this finding. Select the definition name to view full definition details. See [Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/scan-engine-definitions.md) for more information.|
    |**Level of Finding**|Measures the potential severity of the finding on the overall instance on a scale of 0-10.|
    |**Applies to**|A reference to the specific record flagged by the scan \(for example, a business rule, script include, or ACL record\). Select it to open the record directly and review or fix the issue.|
    |**Short Description**|Brief description of the finding|
    |**Finding Details**|What was detected and why|

    The following fields appear on the **Resolution** tab.

<table id="choicetable_rwc_3yq_hhc"><thead><tr><th align="left" id="d41470e158">

Field

</th><th align="left" id="d41470e161">

Description

</th></tr></thead><tbody><tr><td id="d41470e167">

**Estimated Time to Resolve Issue**

</td><td>

Time it will take to resolve the finding

</td></tr><tr><td id="d41470e176">

**Impact to Instance**

</td><td>

-   Finding’s impact level if there is an assigned **Impact to Instance** for the associated definition
-   Ranges from 1 \(minimal\) to 10 \(critical\), as defined in the scan definition. This value helps prioritize findings by business impact. Higher values indicate findings that should be addressed first.


</td></tr><tr><td id="d41470e197">

**Steps to Resolve**

</td><td>

Suggested method for resolving the finding

</td></tr><tr><td id="d41470e206">

**Supporting documentation**

</td><td>

Link to supporting documentation that may help in resolving the finding

</td></tr></tbody>
</table>3.  Apply the recommended changes in the record that triggered the finding.

4.  Submit an exception for review to request to bypass a fix for the finding.

    For more information, refer to [Submit exceptions for Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/submitting-exception-reasons-scan-engine.md).

    The finding will be marked as resolved once the next scan validates the changes.


