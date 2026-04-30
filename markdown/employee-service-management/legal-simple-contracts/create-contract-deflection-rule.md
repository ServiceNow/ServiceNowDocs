---
title: Create a deflection rule for sales contracts
description: Create a deflection rule for providing guidance to requesters for a sales contract based on the specified conditions.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create a deflection rule for sales contracts

Create a deflection rule for providing guidance to requesters for a sales contract based on the specified conditions.

## Before you begin

Role required: sn\_lg\_contracts.contracts\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Deflection Rules**.

2.  Create or modify a deflection rule.

    -   To create a deflection rule, click **New**.
    -   To modify an existing deflection rule, open the deflection rule from the list.
3.  On the form, fill in the fields.

<table id="table_nbm_c44_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the deflection rule.

</td></tr><tr><td>

Order

</td><td>

Order in which the deflection rule is run.If there are multiple rules that meet the conditions from a legal request, a deflection rule with a lower-order number is run for providing the guidance.

</td></tr><tr><td>

Active

</td><td>

Option for marking the deflection rule as active.

</td></tr><tr><td>

Short description

</td><td>

Brief description about the deflection rule.

</td></tr><tr><td>

Table

</td><td>

Table in which the contract requests are saved.The table name is automatically set to **Sales Contract Support \[sn\_lg\_ops\_sales\_contract\_support\]**.

</td></tr><tr><td>

Conditions

</td><td>

Conditions under which the deflection rule applies. For example, to apply a rule when a sales contract has an opportunity size greater than or equal to $50,000, you would enter the following condition:

 **\[Opportunity size\]\[greater than or is\]\[$50,000\]**.

</td></tr><tr><td>

Guidance

</td><td>

Message that is shown to the requester while submitting a sales contract review request to provide guidance.For example, you can add a link to knowledge base article relevant to the legal request or to external web page.

 **Note:** Some formatting options, such as text alignment, underline text, and different fonts and sizes, might not apply in the output.

</td></tr></tbody>
</table>4.  Save the deflection rule.

    -   Save a deflection rule by clicking **Submit**.
    -   Save the changes to an existing deflection rule by clicking **Update**.

