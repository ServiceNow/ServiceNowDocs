---
title: Work with Scan Engine findings
description: You can view and work with open findings resulting from scans.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 3
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Work with Scan Engine findings

You can view and work with open findings resulting from scans.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Enforcement levels and risk impact

Every finding in your instance is evaluated along two critical dimensions to help your team prioritize remediation efforts and maintain compliance standards. Findings are evaluated with a Level of findings and impact to instance ratings.

-   **Level of Findings**: Represents the enforcement behavior which determines how strictly the system reacts to the issue. Such as blocking an action, issuing a warning, or providing informational guidance.
-   **Impact to Instance**: Represents the business and technical risk indicating how harmful the issue could be if left unresolved.

## Examples

These two metrics work together to help teams balance enforcement and risk prioritization, ensuring critical issues are addressed first while maintaining development velocity.

-   ACT level finding with impact to instance of 9: Critical and must be fixed immediately before proceeding. No exceptions.
-   SUGGEST level with impact to instance of 8: High-risk but does not block development. Should still be prioritized for remediation.

<table id="table_scan_findings"><thead><tr><th>

Level of finding

</th><th>

Impact to instance \(typical\)

</th><th>

Severity description

</th><th>

Enforcement behavior / recommended action

</th></tr></thead><tbody><tr><td>

ACT

</td><td>

8–10

</td><td>

Critical issues that can break functionality, cause security vulnerabilities, or block upgrades.

</td><td>

-   The record can not be saved until the code is fixed to meet the requirements in the definition.
-   No exception reason option is available.
-   An override requires admin-level rights or the disabling of the definition.

</td></tr><tr><td>

RECOMMEND

</td><td>

5–7

</td><td>

High severity issues that may degrade performance, stability, or security. Exceptions with governance are allowed.

</td><td>

-   The record can not be saved until the issue is resolved or and exception reason is provided formal approval.
-   For more information, refer to [Submit exceptions for the Scan Engine findings](../concept/submitting-exception-reasons-scan-engine.md).

</td></tr><tr><td>

SUGGEST

</td><td>

2–4

</td><td>

Moderate issues, often related to optimization, maintainability, or best practices.

</td><td>

-   Address during future development cycle
-   Does not block progress
-   Prompts to check for a better solution, if one is available.

</td></tr><tr><td>

REVIEW

</td><td>

0-1

</td><td>

Low impact, informational findings with minimal impact \(e.g., unused fields or minor UI inconsistencies\).

</td><td>

Monitor and optionally fix during future development cycles.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Open Findings**.

2.  Open the record you want to work with by selecting its **Short Description**.

    The finding record displays the following fields.

    |Field|Description|
    |-----|-----------|
    |**Definition**|Displays the scan definition that detected this finding. Select the definition name to view full definition details. See [Scan Engine definitions](../concept/scan-engine-definitions.md) for more information.|
    |**Level of Finding**|Measures the potential severity of the finding on the overall instance on a scale of 0-10.|
    |**Applies to**|A reference to the specific record flagged by the scan \(for example, a business rule, script include, or ACL record\). Select it to open the record directly and review or fix the issue.|
    |**Short Description**|Brief description of the finding|
    |**Finding Details**|What was detected and why|

    The following fields appear on the **Resolution** tab.

<table id="choicetable_rwc_3yq_hhc"><thead><tr><th align="left" id="d39453e340">

Field

</th><th align="left" id="d39453e343">

Description

</th></tr></thead><tbody><tr><td id="d39453e349">

**Estimated Time to Resolve Issue**

</td><td>

Time it will take to resolve the finding

</td></tr><tr><td id="d39453e358">

**Impact to Instance**

</td><td>

-   Finding’s impact level if there is an assigned **Impact to Instance** for the associated definition
-   Ranges from 1 \(minimal\) to 10 \(critical\), as defined in the scan definition. This value helps prioritize findings by business impact. Higher values indicate findings that should be addressed first.


</td></tr><tr><td id="d39453e379">

**Steps to Resolve**

</td><td>

Suggested method for resolving the finding

</td></tr><tr><td id="d39453e388">

**Supporting documentation**

</td><td>

Link to supporting documentation that may help in resolving the finding

</td></tr></tbody>
</table>3.  Apply the recommended changes in the record that triggered the finding.

4.  Submit an exception for review to request to bypass a fix for the finding.

    For more information, refer to [Submit exceptions for the Scan Engine findings](../concept/submitting-exception-reasons-scan-engine.md).

    The finding will be marked as resolved once the next scan validates the changes.


