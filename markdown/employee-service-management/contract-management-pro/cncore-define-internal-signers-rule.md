---
title: Define an internal signatory rule
description: Define an internal signatory rule to map signatories to a template using signatory mappings.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Define an internal signatory rule

Define an internal signatory rule to map signatories to a template using signatory mappings.

## Before you begin

Role required: sn\_cm\_core.contract\_admin and sn\_cm\_core.contract\_config

## About this task

If you want the variables related to a contract request to be available in the condition builder, add the contract request reference to your application table. For more information, see [Provide access to contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Internal Signatory Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_nbm_c44_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of the internal signatory rule.

</td></tr><tr><td>

Template

</td><td>

Template selected from the active and published templates list.

</td></tr><tr><td>

Table

</td><td>

Table that is associated with the selected template. The field is auto-populated when the template is selected.

</td></tr><tr><td>

Description

</td><td>

Description of the internal signatory rule.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the signatory rule is active and available for use.

</td></tr><tr><td>

Order

</td><td>

Order in which the signatory rule is used.

</td></tr><tr><td>

Applies to

</td><td>

Conditions under which the internal signatory rule is selected. For example, if you select an assignment group and configure a user as signatory, that user will be the internal signatory for contract requests that include the selected assignment group.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

5.  In the **Signers Mappings** section, select **New**.

    1.  In the **Participant** field, select a participant.

        **Note:** If signature blocks are configured for the contract template, this field isn’t available.

    2.  In the **Signer** field, select a user from the list.

    3.  Select **Submit**.

6.  Select **Update**.

    **Note:** When more than one internal signatory rule is applicable, the signatory rule with the lowest order is considered.


## Result

An internal signatory rule is created to map a user as an internal signatory for the corresponding contract template.

**Note:** During signatory assignment for contract based on own paper, the **Internal Signatory** rule takes precedence.

-   A user from **Signers mappings** is picked as a signatory.
-   For contract templates configured with participants, when a participant does not meet the **Internal Signatory** rule criteria, a signatory is picked from the user field mapping of the participant list in the template.
-   While creating the signer task for an internal user, check whether the user's legal name is available in the user's employee profile. If no value is provided in the **Legal Name** field, use the user name from the Users \[sys\_user\] table. For more information, see [Employee Profile form](../../employee-center/reference/employee-profile-fieldconfig.md).
-   When no data is found, an empty signatory record is created that can update with the correct signatory details.

