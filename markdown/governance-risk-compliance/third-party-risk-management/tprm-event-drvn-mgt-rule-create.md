---
title: Event-driven management — automate assessment processes
description: Use the Event-driven management feature to configure rules that auto-generate and send questionnaires and doc requests to engagements and third parties. For engagements and third parties that meet the criteria you define, you specify the schedule and the assessment templates. You can automate all assessment types except onboarding.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Event-driven management — automate assessment processes

Use the Event-driven management feature to configure rules that auto-generate and send questionnaires and doc requests to engagements and third parties. For engagements and third parties that meet the criteria you define, you specify the schedule and the assessment templates. You can automate all assessment types except onboarding.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## Procedure

1.  Use either of the following methods to start the process:

    -   Workspace: Select **Workspaces** &gt; **Vendor Management Workspace** and on the **Risk** tab, select the list icon ![](../image/icon-tprm-ws-list.png). In the **Event-driven management** list, select any option: **Active**, **Inactive**, or **All**.
    -   Legacy: Navigate to **All** &gt; **Third-party Risk Management** &gt; **Event-driven management** and then select any option: **Active**, **Inactive**, or **All**.
2.  Select **New** and then fill in the form.

    The following settings appear in sections on the workspace page and as related lists on the legacy form.

<table id="table_cfx_jvb_1zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Meaningful name for the rule that helps others understand its intent and operation.

</td></tr><tr><td>

Number

</td><td>

For each Event-driven management rule, the system auto-assigns a unique ID number that starts with the text EMR. In the history table of rule runs \(executions\), the system auto-assigns a unique ID number for each run that starts with the text EMH.

 The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Business justification

</td><td>

The business reason for defining the automated process.

</td></tr><tr><td>

Technical description

</td><td>

The conditions that trigger the run and the kinds of third parties that are affected.

</td></tr><tr><td colspan="2">

**Scope**: Specify the kind of assessment to generate and the template to use.

</td></tr><tr><td>

Category

</td><td>

-   External assessment: Send questionnaires and doc requests. In the **Applies to** field, you specify whether to send the materials to third parties or to engagements.
-   Reassess engagement: Reassess an existing engagement when the conditions change. For example, let's say that you hear adverse news or have changes in your third-party's supply lines. You might want to reassess the risk by conducting additional due diligence.
-   Reassess engagement for contract renewal: Reassess the risk before your organization renews the contract with a current third party or engagement by conducting due diligence.
-   Offboard engagement with due diligence: Determine if offboarding \(terminating the relationship\) with an engagement is the optimal course of action by conducting due diligence. For example, it might be too risky to switch third parties or engagements even if their current performance doesn’t meet expectations.
-   Offboard engagement with NO due diligence: Request that an engagement be permanently terminated when an engagement ends or you want to switch to a different third party for other reasons. In this case, you typically don't need to conduct additional due diligence. The process does, however, include the normal Inherent Risk Questionnaire \(IRQ\) process to confirm that the services provided by the engagement will no longer continue. For important details, see [Offboarding an engagement without conducting due diligence](../concept/tprm-dd-request-offboard-no-dd.md).


</td></tr><tr><td>

Applies to

</td><td>

This field is editable only if you set the category as **External assessment**.

 Specify whether the questionnaires and doc requests should be sent to third parties or to engagements.

</td></tr><tr><td>

Internal questionnaire template

</td><td>

This field appears if you select any category other than **External assessment**.

 Template that specifies the contents of the Inherent Risk Questionnaire \(IRQ\).

**Note:** If the rule is related to Due Diligence requests and the Smart Assessment Engine is not enabled, the IRQ template will refer to the classic template table \(asmt\_metric\_type\). If the Smart Assessment Engine is enabled, it will refer to the TPRM template table \(sn\_vdr\_risk\_asmt\_sae\_questionnaire\_template\).

</td></tr><tr><td>

Assessment template

</td><td>

This field appears only if you set the category as **External assessment**.

 Template that specifies the questionnaires and doc requests to send.

</td></tr><tr><td colspan="2">

**Run options**: Define the trigger and the schedule for generating the assessments.

</td></tr><tr><td>

Run type

</td><td>

Specify how the rule should be triggered.

 -   **One-time**: Send the third-party risk assessment on the date that you specify in the **Start date** field.
-   **Recurring**: Send the third-party risk assessment on the schedule that you specify with the **Frequency** setting.
-   **On-demand**: The rule runs only when a user selects **Run now**.
 **Note:** Regardless of the **Run type** setting, you can select **Run now** at any time to run the rule immediately. Such an on-demand run doesn’t affect future scheduled runs. In the run history, the **Trigger action** for the run is recorded as **Manual**.

</td></tr><tr><td>

Frequency

</td><td>

This field appears only if you select the **Recurring** run type.

 Specify how often the rule should run.

</td></tr><tr><td>

Start date

</td><td>

This field appears only if you select the **Recurring** or **One-time** run type.

 First date that an active rule is available to run \(depending on the specified filter conditions\). A one-time rule runs on the start date.

</td></tr><tr><td>

End date

</td><td>

This field appears only if you select the **Recurring** run type.

 Last date that an active rule is available to run \(depending on the specified filter conditions\). A rule becomes inactive after the end date.

 If you don’t specify an end date, then the rule continues until you delete or update it.

</td></tr></tbody>
</table>3.  Specify the filter conditions.

    Use the filter editor to specify the conditions that determine which third parties or engagements should receive the questionnaires and doc requests.

    ![Configuring the conditions that trigger an active rule.](../../grc-vendor-risk/image/tprm-emr-filter-conditions.png)

    When you select **Set**, the system applies the filter and displays a link to enable you to view the list of engagements or third parties that match the filter conditions.

4.  Specify how the Third-party Risk \(TPR\) assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\], owner, and contract risk negotiator \[sn\_vdr\_risk\_asmt.contract\_negotiator\] are selected for the engagements or third parties that match the filter conditions.

<table id="choicetable_esz_psj_vzb"><tbody><tr><td id="d270764e469">

**Use last**

</td><td>

Assign the user that most recently performed the function for the engagement.

</td></tr><tr><td id="d270764e478">

**Use onboarding**

</td><td>

Assign the user that most recently performed the function during onboarding for the engagement.

</td></tr><tr><td id="d270764e487">

**Specify now**

</td><td>

When you select this option, a selection box opens to enable you to specify the user.

</td></tr><tr><td id="d270764e496">

**Specify later**

</td><td>

When you select this option, after the rule is saved, you or another user can specify the appropriate TPR assessor or contract risk negotiator later during the workflow. This option doesn’t appear for owner selection.

</td></tr></tbody>
</table>5.  Select **Save** in the workspace or **Submit** in the form.

    -   The system saves the rule.
    -   Regardless of the **Run type** setting, you can select **Run now** at any time to run the rule immediately. Such an on-demand run doesn’t affect future scheduled runs. In the run history, the **Trigger action** for the run is recorded as **Manual**.
    -   The system displays the following additional read-only values on the workspace **Details** tab and on the form.
<table id="table_dlh_qkc_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to activate the rule. By default, newly defined rules aren’t active.

 -   Only active rules with a **Run status** value of **Ready** can run when the specified conditions are met.
-   You can, however, run a rule configured as **On-demand** whether it’s active or not.


</td></tr><tr><td>

Run status

</td><td>

-   **Ready**: The rule is defined and can run as determined by the filter conditions and schedule.

**Note:** Only active rules with a **Run status** value of **Ready** can run when the specified conditions are met.

-   **Running**: The rule is currently running \(questionnaires and document requests are being sent\). For rules that are currently running: The duration between the **Run start** timestamp and the current time indicates how long the rule has been running.
 **Note:** Regardless of the **Run type** setting, you can select **Run now** at any time to run the rule immediately. Such an on-demand run doesn’t affect future scheduled runs. In the run history, the **Trigger action** for the run is recorded as **Manual**.

 If a rule seems to be stuck running for an excessive time:

1.  Go to **Process automation** &gt; **Flow Administration** &gt; **Event Queue**.
2.  Find the platform background task with a name that starts with `sn_vdr` or `sn_tprm` that is in the **error** state.


</td></tr><tr><td>

Next scheduled run

</td><td>

For rules with a recurring **Run type**, the read-only date of the next scheduled run is calculated based on the specified filter conditions and the **Frequency** setting.

</td></tr><tr><td>

Last successful run

</td><td>

Timestamp of the most recent run that is in the **Successful** state.

</td></tr></tbody>
</table>
**Related topics**  


[View the run history for event-driven management rules](tprm-event-drvn-mgt-rule-history.md)

