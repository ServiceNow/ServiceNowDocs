---
title: Understanding Fix records
description: A Fix record represents a single remediation action that resolves one or more findings. Understanding its key fields helps you interpret what a fix does and how much risk it removes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/understanding-fix-records.html
release: australia
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [Fix record, sn\_vul\_fix\_intel, remediation category, risk rating]
breadcrumb: [Use, Fix Intelligence for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Understanding Fix records

A Fix record represents a single remediation action that resolves one or more findings. Understanding its key fields helps you interpret what a fix does and how much risk it removes.

Each fix that Fix Intelligence for SEM identifies is stored as a record in the Fix \(`sn_vul_fix_intel`\) table, and describes a specific remediation action, such as applying a patch, updating an operating system, or changing a configuration.

## Key fields

-   **Number**

    The auto-generated record number \(prefixed `FIX`\).

-   **Description**

    The human-readable summary of the fix. This is the display value for the record.

-   **Remediation category**

    The type of remediation action, such as **Patch Update**, **OS Update**, **Configuration Change**, or **Uninstall Software**.

-   **Finding category**

    The class of findings the fix applies to. In this release, fixes are identified for **host\_vulnerability** findings.

-   **Software package and version**

    The affected software and the version the fix targets, when applicable.

-   **Risk score and risk rating**

    The rolled-up risk of the fix. The numeric **Risk score** is derived into a **Risk rating** from **1 - Critical** to **5 - None**. For more information on roll-up calculators, see [Vulnerability Response Rollup Calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-vuln-rollup-calculator.md).

-   **Findings and assets**

    The rolled-up count of active findings the fix resolves and the count of distinct assets those findings affect.

-   **Active**

    Whether the source still reports the fix.


## Related records

From a Fix record you can reach the records it connects to:

-   **Vulnerable items**: The individual findings the fix remediates. Open a fix to review the vulnerable items linked to it.
-   **Remediation task**: When a remediation task rule groups findings by fix, the resulting remediation task appears on the fix, so you can act on all of the fix's findings as a single unit of work. The fix is also shown on the Remediation Task record. See [Group findings by fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/group-findings-by-fix.md).

**Parent Topic:**[Using Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/using-fix-intel-security-exposure-management.md)

**Related topics**  


[View fixes in USEM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-fixes-in-workspace.md)

[Fix links on findings and vulnerabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/fix-links-on-findings.md)

