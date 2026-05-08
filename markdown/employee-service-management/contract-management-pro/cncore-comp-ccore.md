---
title: Components installed with Contract Management Pro
description: Several types of components are installed with activation of the Contracts Core application that includes the components for Word Document Templates, including tables and user roles.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Contract Management Pro

Several types of components are installed with activation of the Contracts Core application that includes the components for Word Document Templates, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

## Roles

<table id="table_tn1_45f_5xb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th><th>

Group the role is assigned to by default

</th></tr></thead><tbody><tr><td>

Contracts Core user\[sn\_cm\_core.contract\_user\]

</td><td>

This role is required to initiate and track contract execution.

</td><td>

sn\_cm\_obligation.obligation\_user

</td><td>

None

</td></tr><tr><td>

Contracts Core administrator\[sn\_cm\_core.contract\_admin\]

</td><td>

Provides administrative access to Contracts Core and underlying data.

</td><td>

-   sn\_cm\_core.contract\_fulfiller
-   sn\_cm\_core.contract\_config
-   usage\_admin
-   sn\_cm\_pa.pa\_admin role

</td><td>

None

</td></tr><tr><td>

Contracts Core configurator\[sn\_cm\_core.contract\_config\]

</td><td>

Provides access to configure data for contract templates and contract configurations. It doesn’t provide access to the transactional data of Contracts Core.

</td><td>

-   user\_criteria\_admin
-   sn\_cm\_core.contract\_fulfiller
-   view\_changer
-   sn\_doc.writer
-   contract\_manager

</td><td>

Contract Operations

</td></tr><tr><td>

Contracts Core fulfiller\[sn\_cm\_core.contract\_fulfiller\]

</td><td>

This role is required to initiate actions while fulfilling an assigned contract execution. Example: Create revisions, Add Signers, Cancel Signer.

</td><td>

-   sn\_cm\_core.contract\_user
-   sn\_cm\_core.contract\_report\_viewer
-   canvas\_user
-   sn\_cm\_workspace.contract\_workspace\_user
-   approver\_user
-   email\_composer
-   sn\_cm\_core.contract\_report\_viewer
-   sn\_cm\_obligation.obligation\_fulfiller

</td><td>

Contracts Support

</td></tr><tr><td>

Contract report viewer\[sn\_cm\_core.contract\_report\_viewer\]

</td><td>

Provides access to view reports for contract requests and signed contracts data on the Contracts Dashboard.

</td><td>

-   report\_user
-   sn\_cm\_core.contract\_user
-   pa\_viewer

</td><td>

None

</td></tr><tr><td>

Contract report publisher\[sn\_cm\_core.contract\_report\_publisher\]

</td><td>

Provides access to contract requests and signed contracts data for publishing the related reports.

</td><td>

-   report\_publisher
-   sn\_cm\_core.contract\_report\_viewer
-   sn\_cm\_core.contract\_user
-   pa\_power\_user
-   pa\_data\_collector

</td><td>

None

</td></tr><tr><td>

Contract reviewer\[sn\_cm\_core.contract\_reviewer\]

</td><td>

Provides access to review tasks.

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Obligation user\[sn\_cm\_obligation.obligation\_user\]

</td><td>

This role is required to update and submit obligation tasks.

</td><td>

None

</td><td>

None

</td></tr><tr><td>

Obligation fulfiller\[sn\_cm\_obligation.obligation\_fulfiller\]

</td><td>

This role is required to perform actions while managing an obligation. Example: Create obligations,Approve, Reject, or Cancel obligation tasks.

</td><td>

sn\_cm\_obligation.obligation\_user

</td><td>

Obligation Fulfillers

</td></tr><tr><td>

Obligation administrator\[sn\_cm\_obligation.obligation\_admin\]

</td><td>

Provides administrative access to Obligation management and underlying data.

</td><td>

sn\_cm\_obligation.obligation\_fulfiller

</td><td>

None

</td></tr></tbody>
</table>## Tables

<table id="table_k41_45f_5xb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Contracts Core

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

Clause Variation Field\[sn\_cm\_core\_clause\_variation\_field\]

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

Internal Signatory Rule\[sn\_cm\_core\_Signer\_Rule\]

</td><td>

Stores internal signer rule.

</td></tr><tr><td>

Signatory\[sn\_cm\_core\_signer\_task\]

</td><td>

Stores details and the status of the task assigned to the signers.

</td></tr><tr><td>

Contract Type - Contract Model Mapping\[sn\_cm\_core\_contract\_type\_m2m\_contract\_model\]

</td><td>

Store details of contract model mapping.

</td></tr><tr><td>

Contract Document References\[sn\_cm\_core\_document\_reference\]

</td><td>

Store details of document references.

</td></tr><tr><td>

Contract Template Rule\[sn\_cm\_core\_contract\_template\_rule\]

</td><td>

Store details of contract template rules.

</td></tr><tr><td>

Supporting File\[sn\_cm\_core\_supporting\_file\]

</td><td>

Store details of supporting files attached to the non-self-served contract request.

</td></tr><tr><td>

\[sn\_cm\_core\_Integration\_Core\]

Contract Integration

</td><td>

Store details for integration configured for contracts.

</td></tr><tr><td>

\[sn\_cm\_core\_Integration\_Esignature\]

Electronic Signature

</td><td>

Store details of e-signature integrations configured.

</td></tr><tr><td>

Signers Mapping

\[sn\_cm\_core\_Signer\_M2m\_Participant\_Mapping\]

</td><td>

Store details of signer mappings.

</td></tr><tr><td>

Contract Integration

\[sn\_cm\_core\_Integration\_External\_Storage\]

</td><td>

Store details of configured external storage integrations.

</td></tr><tr><td>

Contract Request

\[sn\_cm\_core\_Contract\_Request\]

</td><td>

Store details of the contract requests

</td></tr><tr><td>

External Storage Permission

\[sn\_cm\_core\_external\_storage\_permission\]

</td><td>

Store details of users and their external storage permissions.

</td></tr><tr><td colspan="2">

Obligation management

</td></tr><tr><td>

Obligations

 \[sn\_cm\_obligation\_obligation\]

</td><td>

Store details of obligation records.

</td></tr><tr><td>

Obligation tasks\[sn\_cm\_obligation\_obligation\_task\]

</td><td>

Store details of obligation tasks.

</td></tr></tbody>
</table>## Scheduled jobs

There are several properties that you can use to configure integrations for Contract Management Pro. These properties are used while executing the following scheduled jobs. For more information, see [Properties installed to configure contracts integrations](cncore-properties.md).

<table id="id_zbt_hcj_k1c"><thead><tr><th>

Scheduled job

</th><th>

Data synced to the table

</th><th>

Active

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process external storage permissions for Contracts

</td><td>

External Storage Permission \[sn\_cm\_core\_external\_storage\_permission\]

</td><td>

True

</td><td>

Process external storage permissions for the users.

</td></tr><tr><td>

Validate schedule and create recurring obligation tasks

</td><td>

Obligations

 \[sn\_cm\_obligation\_obligation\_task\]

</td><td>

True

</td><td>

Validate schedule and create recurring obligation tasks

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](../concept/cncore-ref.md)

**Related topics**  


[Components installed with Contract Workspace](cncore-comp-contract-workspace.md)

[Components installed with Analytics Pack for Contract Management Pro](cncore-comp-analytics-pack-cmpro.md)

[Contract request State and Contract document status in Contract Management Pro](cncore-cr-state-status.md)

[Clause Variation form](cncore-cv-form.md)

[Contract Configuration form](cncore-contract-config-form.md)

[Properties installed to configure expiry notifications](cncore-properties-installed.md)

[Properties installed to configure contracts integrations](cncore-properties.md)

[Expiring Contracts Condition form fields](cncore-email-notif-expcont-form.md)

[Action assignment form](cmpro-actn-assignment-form.md)

[UFX Add on Event mapping form](cmpro-ufx-event-map-form.md)

[Obligation form](cncore-obligation-form.md)

[Obligation Management notifications](cncore-ob-mgmt-notification.md)

[Contract Management Pro glossary](../concept/contract-management-pro-glossary.md#)

[Contract Management solutions](cmpro-cml-feature-compare.md)

