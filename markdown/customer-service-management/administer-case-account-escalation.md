---
title: Administering case and account escalation
description: Create escalation templates and escalation severity definitions to control the escalation process for cases and accounts.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Case and account escalation, Administer, Customer Service Management]
---

# Administering case and account escalation

Create escalation templates and escalation severity definitions to control the escalation process for cases and accounts.

## Escalation templates

An escalation template determines how an escalation request is processed by defining the following information:

-   The type of escalation \(case or account\)
-   If approval is required:
    -   If no, the escalation request is automatically approved.
    -   If yes, provide the approver list required by the default approval subflow or provide a different approval subflow.
-   The escalation watch list. Users added to the watch list receive email notifications when an escalation record is updated.

The escalation feature provides two standard escalation templates, one for case escalation and one for account escalation. If needed, users with the system administrator role can modify these templates or create templates.

## Escalation severity

An escalation severity record defines the severity level for the escalation and the color that is used to highlight the escalated case or account record in the user interface. This assigned severity enables agents to easily identify escalated cases and accounts on lists and forms. The escalation feature provides two escalation severity definitions:

-   **High Severity**: Escalated records are highlighted in red.
-   **Medium Severity**: Escalated records are highlighted in orange.

The user interface determines which fields are highlighted for escalated cases and accounts.

<table id="table_zb4_t2n_45b"><thead><tr><th>

User interface

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSM Agent Workspace

</td><td>

Field indicators and field highlights appear on the **Short description** field for escalated cases and on the **Name** field for escalated accounts.**Note:** You can move indicators and highlights to any field that is not a hyperlinked field.

</td></tr><tr><td>

Platform interface

</td><td>

Escalated case and account numbers are indicated with a colored dot on a list and a colored background on a form.

</td></tr></tbody>
</table>![List of cases with escalation details. For the text description, refer to the text that follows.](../image/csm-aw-case-escalation-list.png "CSM Agent Workspace case list with escalated cases")

The CSM Agent Workspace case list shows these escalation details:

-   Number: Automatically generated case number.
-   Short description: Describes the case.
-   Action status: Indicates the status of the case.
-   Contact: Shows the contact person for the case.

In addition to defining the field indicator and field highlight of an escalated case or account, the severity can be used when configuring SLAs. To configure additional escalation severity definitions, the system administrator must configure a new style with the desired color. For more information, see Highlight list fields.

## Escalation SLAs

Escalation SLAs are typically used to govern the frequency of updates required for different types and severities of escalations. An escalation SLA is associated with an escalation severity in the SLA definition. When a user creates an escalation request, the selection in the **Escalation Severity** field determines the SLA for the escalation record. The escalation feature provides the following case and account escalation SLAs. The following table provides information about the escalation SLAs and their descriptions.

<table id="table_ws1_vfn_45b"><thead><tr><th>

Escalation SLAs

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case escalation SLAs

</td><td>

On case escalations, because the escalation corresponds one-to-one with a case, the default SLAs are associated with the case:-   **Escalated case response - 4 hours**: De-escalate the case within four hours.
-   **Escalated case response - 8 hours**: De-escalate the case within eight hours.

 For case escalation, update the SLA reset condition to \`complete the old SLA and start a new one when the case has new comments\`

</td></tr><tr><td>

Account escalation SLAs

</td><td>

On account escalations, because the escalation corresponds to an account which typically doesn’t support SLAs, the SLAs are associated with the escalation.-   **Escalated account response - 4 hours**: De-escalate the account within four hours.
-   **Escalated account response - 8 hours**: De-escalate the account within eight hours.

</td></tr></tbody>
</table>Users with the system administrator role can configure case and account escalation SLAs that are based on escalation attributes such as the escalation type, severity, and trend. Escalation SLAs are stored in the following locations:

-   For account records, on the Escalation form in the **Task SLAs** related list.
-   For case records, on the Case form in the **Task SLAs** related list.

