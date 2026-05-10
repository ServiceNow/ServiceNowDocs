---
title: Components installed with Contract Management Pro for Legal Service Delivery
description: Several types of components are installed with activation of the Contract Management Pro for Legal Service Delivery application which includes the components for Contracts Core and Word Document Templates, including tables and user roles.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Contract Management Pro for Legal Service Delivery

Several types of components are installed with activation of the Contract Management Pro for Legal Service Delivery application which includes the components for Contracts Core and Word Document Templates, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles

**Note:** Some roles in the **Contains roles** column are available with installation of the respective Legal Service Delivery application. For example, roles with an sn\_lg\_matter prefix are added when you install the Legal Matter Management application.

<table id="table_tn1_45f_5xb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Contract Management Pro for Legal Service Delivery configurator sn\_lg\_cnt.contract\_config

</td><td>

Provides access to configure data such as internal signatories and template rules. It does not provide access to data related to legal contract requests submitted.

</td><td>

-   connection\_admin
-   sn\_lg\_ops.legal\_user
-   catalog\_editor
-   sn\_cm\_core.contract\_config

</td></tr><tr><td>

Contract Management Pro for Legal Service Delivery administrator\[sn\_lg\_cnt.contract\_admin\]

</td><td>

Provides the administrative permissions for the Contract Management Pro for Legal Service Delivery app and full access to the underlying data.

</td><td>

-   sn\_lg\_cnt.contract\_config
-   sn\_lg\_cnt.contract\_fulfiller

</td></tr><tr><td>

Contract Management Pro for Legal Service Delivery contract owner\[sn\_lg\_cnt.contract\_owner\]

</td><td>

Manages lifecycle of legal contracts

</td><td>

sn\_cm\_core.contract\_user

</td></tr><tr><td>

Contract Management Pro for Legal Service Delivery fulfiller\[sn\_lg\_cnt.contract\_fulfiller\]

</td><td>

Provides fulfiller access for working on contract requests.

</td><td>

-   sn\_lg\_ops.legal\_user
-   sn\_cm\_core.contract\_fulfiller
-   contract\_manager

</td></tr><tr><td>

Legal User\[sn\_lg\_ops.legal\_user\]

</td><td>

Provides access to submit legal requests and track their progress. Can work on assigned tasks related to matters.

</td><td>

sn\_interview\_temp.reader

</td></tr><tr><td>

Contract user\[sn\_cm\_core.contract\_user\]

</td><td>

This role is required to initiate and track contract execution.

</td><td>

None

</td></tr><tr><td>

Contract administrator\[sn\_cm\_core.contract\_admin\]

</td><td>

Provides administrative access to Contracts Core and underlying data.

</td><td>

-   sn\_cm\_core.contract\_fulfiller
-   sn\_cm\_core.contract\_config
-   usage\_admin

</td></tr><tr><td>

Contract configurator\[sn\_cm\_core.contract\_config\]

</td><td>

Provides access to configure data for contract templates and contract configurations. It doesn’t provide access to the transactional data of Contracts Core.

</td><td>

-   user\_criteria\_admin
-   sn\_cm\_core.contract\_fulfiller
-   view\_changer
-   sn\_doc.writer
-   contract\_manager

</td></tr><tr><td>

Contract fulfiller\[sn\_cm\_core.contract\_fulfiller\]

</td><td>

This role is required to initiate actions while fulfilling an assigned contract execution. Example: Create revisions, Add Signers, Cancel Signer.

</td><td>

sn\_cm\_core.contract\_user

</td></tr></tbody>
</table>## Tables

**Note:** In addition to the following tables, tables specific to practice areas are installed with Legal Request Management. For more information, see [Practice area tables for legal requests](../../legal-request-management/reference/legal-request-pa-tables.md).

<table id="table_k41_45f_5xb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Legal Contracts Repository\[sn\_lg\_cnt\_repository\]

</td><td>

Stores the details of the contract repository.

</td></tr><tr><td>

Clause\[sn\_cm\_core\_clause\]

</td><td>

Stores the details of clause fields.

</td></tr><tr><td>

Imported Clause\[sn\_cm\_core\_imported\_clause\]

</td><td>

Stores data related to imported clauses

</td></tr><tr><td>

Clause mapping\[sn\_cm\_core\_m2m\_clause\_word\_template\]

</td><td>

Stores the details of clause mappings.

</td></tr><tr><td>

Clause Variation\[sn\_cm\_core\_clause\_variation\]

</td><td>

Stores the details of clause variations.

</td></tr><tr><td>

Clause Variation Field\(sn\_cm\_core\_clause\_variation\_field\)​

</td><td>

Stores the details of clause variation fields.

</td></tr><tr><td>

Contract Type\[sn\_cm\_core\_contract\_type\]

</td><td>

Stores the details of contract types.

</td></tr><tr><td>

Contract Document\[sn\_cm\_core\_document\]

</td><td>

Stores the details of contract documents.

</td></tr><tr><td>

Contract Document Revision\[sn\_cm\_core\_document\_revision\]

</td><td>

Stores the details of contract revision.

</td></tr><tr><td>

Contract Type Association\[sn\_cm\_core\_m2m\_contract\_type\_template\]

</td><td>

Stores the details of contract type associations.

</td></tr><tr><td>

Contract Configuration \[sn\_cm\_core\_contract\_configuration\]

</td><td>

Stores details of mapped data that will be added to the contract document and the contract repository where the contracts will be stored.

</td></tr><tr><td>

Contract execution\[sn\_cm\_core\_contract\_execution\]

</td><td>

Stores the details of contract execution.

</td></tr><tr><td>

Contract Repository Mapping\[sn\_cm\_core\_contract\_repository\_mapping\]

</td><td>

Stores the data related to mapping between contract request fields and contract repository fields.

</td></tr><tr><td>

Signer\[sn\_cm\_core\_signer\]

</td><td>

Store data related to the details of signers such as their name, title, email, and signer type.

</td></tr><tr><td>

Signatory\[sn\_cm\_core\_signer\_task\]

</td><td>

Stores details and the status of the task assigned to the signers.

</td></tr><tr><td>

Internal Signatories Mapping\[sn\_cm\_core\_signer\_mapping\]

</td><td>

Stores details of internal signatories.

</td></tr><tr><td>

Contract Type - Contract Model Mapping\[sn\_cm\_core\_contract\_type\_m2m\_contract\_model\]

</td><td>

Stores details of contract type to contract model mapping.

</td></tr><tr><td>

Contract Document References\[sn\_cm\_core\_document\_reference\]

</td><td>

Stores details of Document References.

</td></tr><tr><td>

Contract Template Rule\[sn\_cm\_core\_contract\_template\_rule\]

</td><td>

Stores details of contract template rules.

</td></tr><tr><td>

Supporting File\[sn\_cm\_core\_supporting\_file\]

</td><td>

Store details of supporting files attached to the third-party contract review request.

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro for Legal Service Delivery reference](../concept/snlc-ref-sn-legal-contracts.md)

**Related topics**  


[Third-party Contract Review form](snlc-tpc-intake-fields.md)

