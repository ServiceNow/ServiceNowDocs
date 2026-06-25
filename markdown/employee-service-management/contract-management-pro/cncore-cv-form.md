---
title: Clause Variation form
description: Use the Clause Variation new record form to create or modify a clause variation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-cv-form.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Clause Variation form

Use the Clause Variation new record form to create or modify a clause variation.

<table id="table_lld_cps_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

This field contains an automatically generated unique clause variation number.

</td></tr><tr><td>

Name

</td><td>

Unique name for the clause variation.

</td></tr><tr><td>

Clause

</td><td>

This field is automatically set to the clause name.

</td></tr><tr><td>

Order

</td><td>

Order in which the clause variation is used. If multiple clauses meet a condition, the clause with the lower-order value is chosen first.

</td></tr><tr><td>

Application

</td><td>

This field is automatically set per the application scope setting.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the clause variation is active and available for use.

</td></tr><tr><td>

Applies when

</td><td>

Filter conditions applied to the selected table field and record producer variables to determine which clause variation to use.

</td></tr><tr><td>

Applies to

</td><td>

Criteria to determine the users to whom the clause variation is applicable.For example, if a clause variation is applicable to employees of a specific location, associate the clause variation with user criteria defining only employees of that region.

</td></tr><tr><td>

Applies to user

</td><td>

User to whom the selected user criteria is applicable.

 **Note:**

If no value is selected in the **Applies when** and **Applies to** fields, the clause variation is applicable for the contract template regardless of the user and selected table.

</td></tr><tr><td>

Document

</td><td>

Select **Update** link to upload the document that has the modified content. The selected document should be of .docx file format and should have valid content controls. For more information, see [Add content controls in a Microsoft Word document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-word-doc-tmplt-contls.md) .

</td></tr><tr><td>

Language

</td><td>

This field is automatically set to the default language.

</td></tr><tr><td>

Advanced script

</td><td>

Enables the **Script** field where you can define clause conditions on fields and variables of a table that isn’t directly linked to the contract template table. The condition determines when the clause variation is used in a contract.**Note:** The **Applies when** field is not available when you select the **Advanced script** check box.

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

