---
title: Create an observation for an engagement
description: Create an audit observation to present a summary of problems, discoveries, and recommendations. The audit team can then review the observations to determine if the observation is a reportable issue.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Audit observations in Audit Workspace, Audit Workspace for the Audit supervisor, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Create an observation for an engagement

Create an audit observation to present a summary of problems, discoveries, and recommendations. The audit team can then review the observations to determine if the observation is a reportable issue.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor, sn\_audit.user, sn\_audit\_ws.auditor

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the lists icon \(![List icon](../image/ListsIcon.jpg)\).

3.  Select **All engagements** in the Execution list.

4.  Select the link to the engagement record in the **Name** column.

5.  Select the **Observations** tab.

6.  Select **New**.

7.  On the form, fill in the fields.

<table id="table_nhx_t22_tqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Name

</td><td>

Name of the observation.

</td></tr><tr><td>

Engagement

</td><td>

Engagement associated with this observation.

</td></tr><tr><td>

Source

</td><td>

Source or origin of the observation.

</td></tr><tr><td>

Issue type

</td><td>

Reason for creating the observation. The choices are:-   Control design effectiveness failure
-   Control operative effectiveness failure
-   Control does not exist
-   Control doesn’t meet requirement
-   Other observation


</td></tr><tr><td>

State

</td><td>

State of the observation.

</td></tr><tr><td>

Substate

</td><td>

Substate of the observation.

</td></tr><tr><td>

Priority

</td><td>

Priority of the observation. Choices are:-   1 — Critical
-   2 — High
-   3 — Moderate
-   4 — Low


</td></tr><tr><td>

Description

</td><td>

Detailed description of the observation.

</td></tr><tr><td>

Action plan

</td><td>

Plan for resolving the resulting issue.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Owner

</td><td>

User who creates and is responsible for the observation.

</td></tr><tr><td>

Peer reviewer

</td><td>

One of the auditors responsible for peer review.

</td></tr><tr><td>

Respondent

</td><td>

User responsible for completion of the action plan.Respondent can be the owner of the entity or control associated with the parent engagement.

</td></tr><tr><td>

Reviewer group

</td><td>

Group assigned to review the observation.

</td></tr><tr><td>

Reviewer

</td><td>

User responsible for reviewing the observation.

</td></tr><tr><td>

Watch list

</td><td>

Users interested in following updates to the observation.

</td></tr><tr><td class="sub-head" colspan="2">

Details

</td></tr><tr><td>

Control

</td><td>

Control associated with the observation.

</td></tr><tr><td>

Control Objective

</td><td>

Control objective associated with the observation.

</td></tr><tr><td>

Entity

</td><td>

Entity associated with the observation.

</td></tr><tr><td>

Audit task

</td><td>

Audit task associated with the observation.

</td></tr><tr><td class="sub-head" colspan="2">

Results

</td></tr><tr><td>

Result

</td><td>

Result of the observation. The choices are as follows:-   Track as an observation
-   Track as a recommendation
-   Track as a best practice
-   Confirmed as a new issue
-   Confirmed as an existing issue
-   No action required


</td></tr><tr><td>

Explanation

</td><td>

Explanation for the selected result.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Notes about the observation. Work notes are visible to users who are assigned to the observation.

</td></tr><tr><td>

Additional comments

</td><td>

Public information about the observation.

</td></tr><tr><td class="sub-head" colspan="2">

Security

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.

</td></tr></tbody>
</table>    -   **Confidentiality flag to control access of audit records**

        You can set the confidentiality flag at the record level for an issue, engagement, observation, control test, activity, interview, and walkthrough records. The users whom you determine to view and update these records are confidential users.

        When the **Confidentiality** option is selected, a list of users who can be an engagement lead, auditors, and approvers are auto-populated as **Confidential users**.

        You can add more audit users or GRC business users to the list or remove some of the existing users based on your access control criteria and can set them as confidential users.

        Additionally, you can also add random users to the record, who are neither audit users nor GRC business users. However, an email notification is sent to all confidential users who have neither an audit user nor a GRC business user role intimating them to acquire the confidential role \(sn\_grc.confidential\_user\) from the admin if they are to access the record.

        You can also select groups as **Confidential groups** who can access the record as well. For more information, see Confidential records in GRC common features.

        To enable the Confidentiality property at the system level:

        1.  Navigate to **System Properties** &gt; **All Properties**.
        2.  Select **sn\_grc.enable\_record\_confidentiality** system property.
        3.  Enter **true** in the **Value** field. This action enables record level confidentiality.
        4.  Select **Update**.
8.  Select **Save**.

    You can monitor the state of the observation record in the **State** banner of the default Overview page as the record progresses through the different states.


