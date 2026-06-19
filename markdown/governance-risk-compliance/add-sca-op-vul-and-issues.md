---
title: Log operational vulnerabilities and issues
description: Optionally document operational weaknesses and link issues identified from the scenario analysis results to support remediation tracking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-sca-op-vul-and-issues.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Scenario Analysis, Operational Resilience, operational vulnerabilities, issues, remediation]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Log operational vulnerabilities and issues

Optionally document operational weaknesses and link issues identified from the scenario analysis results to support remediation tracking.

## Before you begin

Role required: **sn\_oper\_res.admin**, **sn\_oper\_res.manager**

## About this task

Steps to identify operational vulnerabilities and log issues are optional. They are available after the **Treatment Decision** step is marked as complete. Skipping either step does not block the **Complete analysis** action. Issues are tracked separately from the analysis itself.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and open the Scenario Analysis record form.

2.  In the Playbook stage panel, select **Operational Vulnerabilities**.

3.  Select **New** to document a weakness identified from the results.

4.  Enter a **Name** for the vulnerability and confirm the auto-populated **Source record**, which points to the current scenario analysis.

    The **Number** is generated automatically with the `ORV` prefix. The created vulnerability follows the standard operational vulnerability life cycle: New, Assessment, Treatment, Pending approval, Approved, Closed, Canceled. For more information, see [Operational vulnerability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/exploring-op-vul.md).

    **Note:** You can only create vulnerabilities from this step. To pull in an existing operational vulnerability, use the operational vulnerability list view directly.

    \[Omitted image "sca-op-vulnerabilities-stage-with-record.png"\] Alt text: Operational Vulnerabilities step listing one row with Number, Name, and Source record set to the current scenario analysis.

5.  Select **Mark as complete**, or select **Skip this step** if no vulnerabilities apply.

    **Note:** This step is optional. Skipping does not block the **Complete analysis** action.

6.  In the Playbook stage panel, select **Issues**.

7.  Select **New** to create an issue.

8.  Review the **Issue**, **Number**, **Issue source**, and **Issue type** fields for each linked issue.

    Issues can be tracked separately from this analysis.

    **Note:** Both the **Operational Vulnerabilities** and the **Issues** stages are editable until you select **Complete analysis** on the scenario analysis record. After **Complete analysis** is selected, both stages move to read-only mode and no new vulnerabilities or issues can be added from the playbook.

9.  Select **Mark as Complete** if at least one issue is linked.

    1.  Select **Skip** if no issues apply.

    The **Mark as Complete** button remains inactive until an issue is added, so **Skip** is the only way to leave the step empty.

    \[Omitted image "sca-issues-stage-skip-option.png"\] Alt text: Scenario Issues step with an empty list, the Complete Analysis button,Skip button, and \(an inactive\) Mark as Complete button shown on the form.


## Result

Operational vulnerabilities and issues have been recorded or skipped. The **Complete analysis** action is now available. For more information on completing Scenario analysis, see [Mark the scenario analysis as complete](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-analysis.md).

