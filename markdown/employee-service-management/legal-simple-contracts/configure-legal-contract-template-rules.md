---
title: Configure a rule for selecting a legal contract template
description: Configure a rule to identify and use the correct legal contract document template based on the submitted legal request and generate a contract document for the requester.
locale: en-US
release: australia
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legal contract templates, Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure a rule for selecting a legal contract template

Configure a rule to identify and use the correct legal contract document template based on the submitted legal request and generate a contract document for the requester.

## Before you begin

Role required: sn\_lg\_ops.legal\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Template Rules**.

2.  Configure or modify a contract template rule.

    -   To configure a new contract template rule, click **New**.
    -   To modify an existing contract template rule, open the contract template rule from the list.
3.  On the form, fill in the fields.

<table id="table_nbm_c44_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the contract template rule.

</td></tr><tr><td>

Active

</td><td>

Option for marking the rule as active.

</td></tr><tr><td>

Description

</td><td>

 

</td></tr><tr><td>

Contracts table

</td><td>

Table in which the contract requests are saved.

</td></tr><tr><td>

Condition

</td><td>

Conditions under which the contract template selection rule applies. For example, to apply a rule when a legal request is submitted in an NDA category, you would enter the following condition:

 **\[Category\]\[is\]\[NDA\]**.

</td></tr><tr><td>

Document template

</td><td>

Published and active document template that will be picked for generating the contract document when the specified conditions are met.

</td></tr><tr><td>

Execution order

</td><td>

Order in which the selection rule is run.If there are multiple rules that meet the conditions from a legal request, a template rule with a lower-order number is run for selecting the template.

</td></tr></tbody>
</table>4.  Save the contract template rule.

    -   Save a contract template rule by clicking **Submit**.
    -   Save the changes to an existing contract template rule by clicking **Update**.
    The Internal Signatories Mapping related list appears.

5.  Map internal signers.

    1.  In the Internal Signatories Mapping related list, click **New**.

    2.  In the **Internal Signer** field, select a user from the list of internal signers.

        The list shows all users from the Signer \[sn\_lg\_contracts\_signer\] table.

    3.  In the Participant field, select user from the list of participants added in the template selected in the **Document template** field.

    4.  Click **Submit**.


