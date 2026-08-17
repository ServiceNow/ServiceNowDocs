---
title: Prioritize remediation by fix
description: Use the Fix data and Security Exposure Management dashboards to focus first on the fixes that resolve the most findings and remove the most risk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/prioritize-remediation-by-fix.html
release: australia
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [prioritize by fix, Findings with fix identified, Top fixes by finding count, dashboards]
breadcrumb: [Use, Fix Intelligence for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Prioritize remediation by fix

Use the Fix data and Security Exposure Management dashboards to focus first on the fixes that resolve the most findings and remove the most risk.

## Before you begin

Role required: `sn_vul_fix.read`, or a Vulnerability Response role that contains it.

Prerequisites:

-   Fix Intelligence for SEM has identified fixes and rolled up their risk scores.

## About this task

Because one fix can resolve many findings across many assets, prioritizing by fix often removes more risk per action than working finding by finding. Fix Intelligence for SEM adds widgets and rolled-up fix metrics that support this. For general prioritization guidance in USEM, see the linked topics; this task covers the fix-specific view.

## Procedure

1.  Open the **Remediation overview** and select the **Fix Intelligence** tab.

    The tab shows the following:

    -   Findings that have a fix identified and the ones that don't
    -   Number of unique fixes
    -   breakdowns of findings that have a fix by **Risk rating** and by **Remediation category**
    -   Top 5 fixes to reduce critical risk \(sorted by rolled-up risk score\)
    -   Top 5 common fixes sorted by active findings.
2.  Use **Top 5 fixes to reduce critical risk** to find the fixes that remove the most risk, and **Top 5 common fixes** to find the fixes that resolve the most or greatest number of findings.

    Select **View All** on either list to see all fixes sorted accordingly.

3.  In the Fix list, sort by **Risk score** or filter by **Risk rating** to surface the fixes that remove the most risk.

    For more information on roll-up calculators, see [Vulnerability Response Rollup Calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-vuln-rollup-calculator.md).

4.  Open a candidate fix and review its findings and assets to confirm scope and impact.

5.  Use the **Fix Intelligence** section on a configurable **Findings View** dashboard to see fixes for a specific slice of findings, such as approaching-target or critical-risk findings.

    The section shows how many findings in that dashboard have a fix identified, the unique fixes, the top fixes, and the top remediation categories.

6.  Plan remediation for the selected fixes, optionally grouping their findings into a remediation task.

    See [Group findings by fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/group-findings-by-fix.md).


## Result

You have a prioritized set of fixes to remediate, ordered by the findings and risk they address.

**Parent Topic:**[Using Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/using-fix-intel-security-exposure-management.md)

**Related topics**  


[Remediation view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-workspaces-ui-remediation-module.md)

[Prioritizing vulnerabilities and other findings using roll-up calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-prioritizing-vulnerabilities-other-findings.md)

