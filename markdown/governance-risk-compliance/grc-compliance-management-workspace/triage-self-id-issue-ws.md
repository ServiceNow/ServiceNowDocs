---
title: Triage a self-identified issue using the Compliance Workspace
description: After an issue has been identified and submitted by employees or business users via the Service Portal, the issue triage process begins. The actual problem is identified and assigned to the appropriate owner for prioritization and resolution in the Compliance Workspace.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Manage issues using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Triage a self-identified issue using the Compliance Workspace

After an issue has been identified and submitted by employees or business users via the Service Portal, the issue triage process begins. The actual problem is identified and assigned to the appropriate owner for prioritization and resolution in the Compliance Workspace.

## Before you begin

Role required:

-   sn\_compliance.manager
-   sn\_compliance.user
-   sn\_grc\_advanced.issue\_triage\_manager
-   sn\_grc\_advanced.issue\_triage\_user

## About this task

Your employees and business users within your company can self-identify an issue and submit it via the ServiceNow® Service Portal. Following submission, a triage issue is automatically created. For more information, see [Report self-identified issues via the Service Portal](../../grc-policy-and-compliance/task/create-self-identified-issues.md).

The assigned triage teams identify whether the self-identified issues are actual reported issues, risk events, or observations to be tracked and possibly closed out as noise.

**Note:** In the initial release, only self-identified issues are handled by the triage process. In a later release, system-generated issues, such as those caused by indicator or attestation failures, will also be triaged.

The end-to-end flow of the issue triage life cycle is illustrated and described here.

![Issue triage](../image/issue-triage_lifecycle-ws.png "Issue triage life cycle")

<table id="table_exh_nm3_b4b"><thead><tr><th>

Stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create and assign triage issue

</td><td>

An employee identifies an issue related to an entity, control, policy, authority document, process, or risk, and submits a triage request in the ServiceNow Service Portal. Based on the type of issue submitted and an issue assignment rule, the issue is assigned to a triage team and a triage owner.

</td></tr><tr><td>

Analyze triage issue

</td><td>

The triage team decides whether the issue should be analyzed as an actual issue or risk event, or tracked as a recommendation for a policy or for optimizing a process. During analysis, the triage team may request more information from the issue creator. The team may also optionally send the issue to the compliance manager, risk manager, or triage manager with a triage result.

 Possible results include:

-   Confirmed as a new issue
-   Confirmed as an existing issue
-   Confirmed as a risk event
-   Track as a recommendation
-   Close as a non-issue/No action required

</td></tr><tr><td>

Review triage issue

</td><td>

The Review state is optional. The team may send the issue and result to the compliance manager, risk manager, or triage manager for review. They may also request more information from the triage owner.The compliance manager, risk manager, or triage manager decides whether the issue should be confirmed as an issue or risk event, tracked as a recommendation, or closed as a non-issue.

</td></tr><tr><td>

Close triage issue

</td><td>

If the issue had been determined to be an actual issue or risk event, those records are created, or the triage issue is added to an existing issue.When the triage process is completed, the triage issue is automatically closed. The issue can also be manually closed by the manager and triage team.

</td></tr></tbody>
</table>The following user roles are involved in the issue triage process.

<table id="table_dpt_mkr_x4b"><thead><tr><th>

Persona/Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business user/Employee

</td><td>

Ability to report issue.

</td></tr><tr><td>

-   Compliance user/manager
-   Risk user/manager
-   Triage user/manager

</td><td>

Ability to triage and review issues

</td></tr><tr><td>

Issue manager

</td><td>

Ability to manage and review the reportable issue

</td></tr><tr><td>

Issue owner

</td><td>

Ability to resolve the reportable issue assigned to them

</td></tr></tbody>
</table>**Note:** The triage user/manager and Issue manager roles were introduced in GRC: Policy and Compliance Management version 11.1.0.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Issue Triage** &gt; **My Triage Issues** or **Risk** &gt; **Issue Triage** &gt; **My Triage Issues**.

    The list shows triage issues previously created and assigned to you.

2.  Click the number of the issue that you want to triage.

    **Note:** The **Classification** field is automatically pre-filled based on the **Issue type** selected. Similarly, an assignment rule called sn\_grc\_advanced\_issue\_triage runs and pre-fills the **Triage group**. This rule uses the **Source** and **Classification** to determine the group to which the triage is assigned. Assignment rules also handle issue triages in Risk Management and triages where the **Classification** is set to **Other** \(which is initially unknown\). For the second use case, you must manually set the **Triage group** to **Risk** or **Compliance**.

3.  When you are ready for triage of this issue to begin, select a **Triage owner** and click **Analyze**.

    The assigned Triage owner can open the issue and begin analyzing the issue.

4.  During analysis, the triage owner can perform several tasks.

    The owner may, for example, decide that the issue is misclassified and can change the **Issue type**. This action could result in the change of Triage group and Triage owner. In this example, the assignment rule runs in the background and the issue is removed from the current owner's queue.

5.  The triage owner can also perform the following actions:

    -   Click **Request Information** to request additional information from the issue submitter.
    -   Click **Request Review** to request a review from the user identified in the **Reviewer** field. That user can open and review the issue by navigating to **Policy and Compliance** &gt; **Issue Triage** &gt; **My Pending Reviews**.
    -   Select the **Details** related list to provide additional enrichment to the issue.
6.  After it has been determined what action \(if any\) should be performed on the issue, the triage owner can select a result of the analysis from the **Results** related list.

    **Note:** The options available in the **Result** field depend on the **Issue type** identified for this issue. For example, if you select **Control design effectiveness failure** as the **Issue type**, the following results may be selected.

    If you select a result, such as **Confirmed as a new compliance issue**, which requires more action than simple observation, additional analysis fields appear.

    If the result is **Confirmed as an existing compliance issue**, then an **Existing issue** field appears where you must identify the existing issue that you are referring to.

7.  When the issue triage is complete, the triage owner can click **Complete Triage**.

    **Note:** If the issue is out for review, the reviewer can also click **Complete Triage** to complete the triage and create an actual issue.

    The issue triage transitions to the **Closed** state and a link to the issue displays at the top of the screen.

8.  The issue can be analyzed using the usual issue management procedures.

    One significant change on the **Issue** form is the addition of an **Issue Triages** related list. Opening the triage record provides the analyst with the details of the triage that resulted in the creation of this issue.


