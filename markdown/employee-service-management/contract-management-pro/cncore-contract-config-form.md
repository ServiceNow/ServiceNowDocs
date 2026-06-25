---
title: Contract Configuration form
description: Use the Contract Configuration New Record form to create or modify a contract configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-contract-config-form.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-03-12"
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
</table>**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Clause Variation form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

