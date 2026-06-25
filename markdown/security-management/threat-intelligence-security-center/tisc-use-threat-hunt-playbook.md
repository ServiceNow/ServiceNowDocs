---
title: Use the Threat Hunting Playbook
description: Run threat hunt on a Case record — from capturing the hunt hypothesis through to creating a Security incident or reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-use-threat-hunt-playbook.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 6
keywords: [tisc, threat hunting, playbook, intake, triage, scoping, threat hunt, review outcomes, post hunt]
breadcrumb: [Threat Hunting Playbook, Using playbooks, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Use the Threat Hunting Playbook

Run threat hunt on a Case record — from capturing the hunt hypothesis through to creating a Security incident or reporting.

## Before you begin

Role required: sn\_sec\_tisc.analyst

Confirm that the Threat Hunting playbook is active. See [Activate the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-activate-threat-hunt-playbook.md) for the activation details.

For the Scoping stage, MITRE data must be present in the instance. MITRE data sources are shipped in a deactivated state — an administrator must activate and run a MITRE data source before TTPs can be selected.

## About this task

The playbook progresses through six stages in sequence. Each stage has specific actions, and some actions are restricted to the case owner. You can cancel the playbook any time during its execution.

**Important:** Manual actions performed during the playbook execution can result in conflicts or duplication of the activities on the Case.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  To initiate the Threat Hunting playbook on a Case, create a Case with the **Case Type** set to **Threat Hunting** and **Status** set to **Draft**.

    You can also attach the playbook manually and initiate the playbook. For more information, see [Add the Threat Hunting Playbook to a Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-add-playbook-manually.md).

5.  Open the Case record and select the **Playbooks**.

6.  In the Intake stage, provide the hunt hypothesis, set the assignee, and link the entities to investigate.

    |Field|Description|
    |-----|-----------|
    |**Case Record Details**|
    |**Description**|Enter the hunt hypothesis, for example, the suspected adversary behavior, the observables of interest, and the expected outcome of the hunt.|
    |**Assignment group**|The group responsible for the Case.|
    |**Assigned to**|The user set as the case owner. The case owner is the only user who can transition the playbook to the next stage.|
    |**Linked Entities Summary**|
    |**Navigate to Artifacts**|Redirects to the **Artifacts** tab to add entities.|
    |**Update Case Details**|Saves your changes. The playbook remains on the Intake stage so that you can continue refining the hypothesis or linking more entities.|
    |**Done**|Available to the case owner. Transitions the playbook to the **Triage** stage.|

7.  In the Triage stage, as a Case owner, review the hunt hypothesis and either approve it to continue or reject it to cancel the hunt.

    If you're not the case owner, you can only add to the description and update the case details.

    |Field|Description|
    |-----|-----------|
    |**Description**|Displays the hypothesis from Intake. Any analyst with access to the Case can update it and select **Update Case Details**.|
    |**Approve Hypothesis**|Available to the Case owner. Transitions the playbook to the **Scoping** stage. The decision is recorded as a work note on the Case.|
    |**Reject Hypothesis**|Available to the Case owner. Cancels the playbook and sets the Case status to **Cancelled**. The decision is recorded as a work note on the Case.|

8.  In the Scoping stage, provide the MITRE TTPs, define the hunt scenarios, and create the hunt tasks that assign work to analysts.

    1.  In **Select relevant TTPs**, select the relevant MITRE TTPs from the list.

        All executed MITRE TTPs are listed here.

<table><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

**MITRE TTPs**

</td><td>

Select from the relevant MITRE TTPs from the list. All your executed MITRE TTPs are listed here.**Note:** You must execute the MITRE-related data source to fetch it in the instance.

</td></tr><tr><td>

**Skip**

</td><td>

Skips the activity, for example when no TTPs apply.

</td></tr><tr><td>

**Confirm**

</td><td>

Adds the selected techniques and its matrix and tactic metadata to the case description and marks the activity complete.

</td></tr></tbody>
</table>    2.  In **Provide Hunt Scenarios**, analysts with Case access can provide or update scenarios for the case owner to approve.

        | | |
        |---|---|
        |**Description**|Enter the scenarios that the analysts will investigate.|
        |**Due date**|Provide a due date for the Case.|
        |**Update Case Details**|Updates the case details with your entries.|
        |**Approve Scenarios** / **Reject Scenarios**|Case-owner actions. **Approve Scenarios** proceeds to the **Create Hunt Tasks** activity. **Reject Scenarios** cancels the playbook and the Case.|

    3.  In **Create Hunt Tasks**, create hunt tasks for the investigation.

        | | |
        |---|---|
        |**New Hunt Task**|Creates a new hunt task for an approved scenario and assigns it to an analyst.|
        |**Done**|Available to the case owner when the hunt tasks are created. Transitions the playbook to the **Hunt** stage.|

9.  In the Hunt stage, track the progress of the hunt tasks, record analysis and findings, and complete the hunt.

    |Field|Description|
    |-----|-----------|
    |**Provide Hunt findings**|Aggregated findings from all hunt tasks. Analysts can update findings on individual hunt tasks; updates flow back into this field.|
    |**Summary of case tasks**|Summary of each hunt task grouped by state.|
    |**Update Case Details**|Saves your changes. The playbook remains on the Hunt stage so that team members can continue to add findings.|
    |**Complete Hunt**|Available to the case owner. Transitions the playbook to the **Review Outcomes** stage.|

10. In the Review and Confirm Outcomes stage, review the aggregated insights and the related records before advancing to **Post Hunt**.

    |Field|Description|
    |-----|-----------|
    |**Notes**|Notes for the threat hunt.|
    |**Recommendations or Actions**|Recommended next steps derived from the hunt.|
    |**Analysis and Findings**|Aggregated findings from all hunt tasks. Read-only in this stage.|
    |**Closure Summary**|Summary of how the hunt concluded.|
    |**Update Case Details**|Saves your changes. The playbook remains on the Review and Confirm Outcomes stage so that team members can continue to add findings.|
    |**Confirm Outcomes**|Available to the case owner. Transitions the playbook to the **Post Hunt** stage.|

11. In the Post Hunt stage, optionally escalate the hunt to a Security Incident or generate a report, and then finalize the playbook.

    |Action|Description|
    |------|-----------|
    |**Create Security Incident**|Optionally available to the users with write access on the Security Incident table. Escalates the hunt findings to a Security Incident through the **Create Security Incident** modal. The Security Incident is linked to the Case automatically.|
    |**View Case Reports**|Redirects to the **Case Reports** tab where you can create report.|
    |**Complete Playbook**|Finalizes the playbook. The playbook is marked as complete on the Case record and can't be re-initiated on the same Case.|


**Parent Topic:**[Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.md)

**Related topics**  


[Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.md)

[Activate the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-activate-threat-hunt-playbook.md)

[Add the Threat Hunting Playbook to a Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-add-playbook-manually.md)

[Associate MITRE Techniques to a Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-associate-mitre-technique.md)

[Creating case task using Threat Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-create-case-task.md)

