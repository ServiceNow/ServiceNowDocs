---
title: Contract Configuration form
description: Use the Contract Configuration New Record form to create or modify a contract configurations.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract Configuration form

Use the Contract Configuration New Record form to create or modify a contract configurations.

<table id="table_w5n_3qh_hbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the contract configuration.

</td></tr><tr><td>

Request Table

</td><td>

Table with which you want to associate the contract configuration.**Note:** The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to have the configuration on a different table.

</td></tr><tr><td>

Contract Repository

</td><td>

Repository where the contract records should be created.

</td></tr><tr><td>

Document type

</td><td>

Indicates how the contract document is generated. The available values are:-   Word template: Contract document is generated from Word document templates for the contract configuration.
-   Third-party contract: Contract documents is generated from the documents attached in the third-party contract request.

</td></tr><tr><td>

Template

</td><td>

The contract template to be used to generate a standard contract with predefined content. This field appears only when Word template is selected from **Document type**.

</td></tr><tr><td>

Application

</td><td>

This field is automatically set per the application scope setting.

</td></tr><tr><td>

Request type

</td><td>

Type of request the template rule is applicable to.For contract requests, select **New Contract**; for amendment requests, select **Amendment**.

</td></tr><tr><td>

Active

</td><td>

Option to make the contract configuration active.

</td></tr><tr><td>

Order

</td><td>

Order in which the selection rule is run.If multiple rules meet the conditions from a contract request, the rule with the lowest order number is run first for selecting the configuration.

</td></tr><tr><td>

Applies to

</td><td>

Conditions under which the contract configuration is applied. For example, to apply a configuration when a contract request is submitted in the Non-disclosure agreement category, you would enter the following condition: **\[Category\]\[is\]\[ Non-disclosure agreement\]**.

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](../concept/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro](cncore-comp-ccore.md)

[Components installed with Contract Workspace](cncore-comp-contract-workspace.md)

[Components installed with Analytics Pack for Contract Management Pro](cncore-comp-analytics-pack-cmpro.md)

[Contract request State and Contract document status in Contract Management Pro](cncore-cr-state-status.md)

[Clause Variation form](cncore-cv-form.md)

[Properties installed to configure expiry notifications](cncore-properties-installed.md)

[Properties installed to configure contracts integrations](cncore-properties.md)

[Expiring Contracts Condition form fields](cncore-email-notif-expcont-form.md)

[Action assignment form](cmpro-actn-assignment-form.md)

[UFX Add on Event mapping form](cmpro-ufx-event-map-form.md)

[Obligation form](cncore-obligation-form.md)

[Obligation Management notifications](cncore-ob-mgmt-notification.md)

[Contract Management Pro glossary](../concept/contract-management-pro-glossary.md#)

[Contract Management solutions](cmpro-cml-feature-compare.md)

