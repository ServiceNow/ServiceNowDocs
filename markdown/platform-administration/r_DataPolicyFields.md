---
title: Data policy fields
description: These fields appear on the Data Policy form and related forms.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a data policy, Data policy, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Data policy fields

These fields appear on the Data Policy form and related forms.

<table id="table_cml_whn_jq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table to which this policy applies.

 **Note:** The list shows only tables and database views that are in the same scope as the data policy.

</td></tr><tr><td>

Application

</td><td>

Application that contains this data policy.

</td></tr><tr><td>

Inherit

</td><td>

If selected, applies this data policy to tables that extend the specified table. For example, incident, problem, and change tables all extend the task table, therefore selecting Inherit on a data policy defined for task would apply the data policy to them as well.

</td></tr><tr><td>

Reverse if false

</td><td>

If selected, the data policy action is reversed when the conditions evaluate to false. For example, when the conditions are true, then actions are taken and when they change to false, the actions are reversed.

</td></tr><tr><td>

Active

</td><td>

If selected, the data policy is used.

</td></tr><tr><td>

Short description

</td><td>

A short description that identifies the policy.

</td></tr><tr><td>

Description

</td><td>

A detailed description of the policy.

</td></tr><tr><td>

Apply to import sets

</td><td>

If selected, the data policy applies to data brought into the system from import sets. This option also applies to web service import sets.

</td></tr><tr><td>

Apply to SOAP

</td><td>

If selected, the data policy applies to data brought into the system from a SOAP web service. Scripted SOAP web services are not affected. This field does not affect data policy interaction with REST web services.

</td></tr><tr><td>

Use as UI Policy on client

</td><td>

If selected, enforces the data policy on the UI using the UI policy engine.

</td></tr></tbody>
</table><table id="table_qps_jnn_jq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table on which the data policy action applies.

</td></tr><tr><td>

Field name

</td><td>

The field from the specified table to which the data policy will apply.

</td></tr><tr><td>

Read Only

</td><td>

How the data policy affects the read only state of the field. Choices are:-   Leave alone
-   True
-   False

</td></tr><tr><td>

Mandatory

</td><td>

How the data policy affects the mandatory state of the field. Choices are:

-   Leave alone
-   True
-   False

 **Note:** For tables that are in a different scope than the data policy record, you cannot make a field mandatory.

</td></tr></tbody>
</table>