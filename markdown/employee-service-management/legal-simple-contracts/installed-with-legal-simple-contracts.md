---
title: Components installed with Legal Simple Contracts
description: Several types of components are installed with activation of the Legal Simple Contracts application, including tables and user roles.
locale: en-US
release: australia
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Simple Contracts

Several types of components are installed with activation of the Legal Simple Contracts application, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Contracts Administrator\[sn\_lg\_contracts.contracts\_admin\]

</td><td>

Application-specific administrator role for the Legal Simple Contracts app having the administrative access for the app and full access to the underlying data.

</td><td>

-   sn\_lg\_contracts.contracts\_config
-   sn\_lg\_contracts.contracts\_fulfiller

</td></tr><tr><td>

Contracts Configurator\[sn\_lg\_contracts.contracts\_config\]

</td><td>

Provides access to configure data such as document templates, internal signatories, template rules. It does not provide access to transactional data of requests and matters.

</td><td>

-   connection\_admin
-   sn\_docusign\_spoke.docusign\_user
-   sn\_adobesign\_spoke.Adobe\_Sign\_User
-   sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Contracts Fulfiller\[sn\_lg\_contracts.contracts\_fulfiller\]

</td><td>

Provides the fulfiller access for working on assigned contract requests.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Sales User\[sn\_lg\_contracts.sales\_user\]

</td><td>

Provides the read access on sales opportunities and accounts data.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr></tbody>
</table>## Scheduled data imports

<table id="table_cqf_23y_5qb"><thead><tr><th>

Scheduled data imports

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales Representatives Scheduled Data Import

</td><td>

Pulls all sales representatives data from the CRM system into the Sales Representative \[sn\_lg\_contracts\_sales\_representative\] table.This is the main scheduled data import job that is scheduled to run once daily at the set time.

</td></tr><tr><td>

Sales Accounts Scheduled Data Import

</td><td>

Pulls Accounts associated with the sales representative into the Sales Account \[sn\_lg\_contracts\_sales\_account\] table.This job runs after the Sales Representatives Scheduled Data Import job finishes.

​

</td></tr><tr><td>

Sales Opportunities Scheduled Data Import

</td><td>

Pulls Opportunities associated with the sales representative into the Sales Opportunity \[sn\_lg\_contracts\_sales\_opportunity\] table.This job runs after the Sales Accounts Scheduled Data Import job finishes.

</td></tr></tbody>
</table>## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract Request Mapping \[sn\_lg\_contracts\_repository\_request\_m2m\]

</td><td>

Stores the details of the relationship between a request in the General Contract Support \[sn\_lg\_ops\_general\_contract\_support\] table and a contract record in the Legal Contract \[sn\_lg\_contracts\_repository\] table.

</td></tr><tr><td>

Contract Template Rule \[sn\_lg\_contracts\_template\_rule\]

</td><td>

Stores rules to identify a template contract document based on the input data in a request.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Contract Type\[sn\_lg\_contracts\_type\]

</td><td>

Stores the types of contract.

</td></tr><tr><td>

Deflection Rule \[sn\_lg\_contracts\_deflection\_rule\]

</td><td>

Stores deflection rules for sales contract reviews to provide resolution to the requesters based on the entered information in the request, without the need to submit the request.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Document Revision \[sn\_lg\_contracts\_contract\_draft\]

</td><td>

Stores the first draft and other revisions of a contract document for a legal request.

</td></tr><tr><td>

Legal Contract \[sn\_lg\_contracts\_repository\]

</td><td>

Stores all signed contract documents.

</td></tr><tr><td>

Sales Account\[sn\_lg\_contracts\_sales\_account\]

</td><td>

Stores information about sales accounts that belong to sales representatives.

</td></tr><tr><td>

Sales Account Import Set\[sn\_lg\_contracts\_sales\_account\_import\_set\]

</td><td>

Staging table for sales account records pulled from the Microsoft Dynamics CRM system.

</td></tr><tr><td>

Sales Dynamics Staging Data\[sn\_lg\_contracts\_sales\_dynamics\_staging\_data\]

</td><td>

Stores data imported from the CRM system. The data is pulled from the Microsoft Dynamics CRM system using a scheduled import set job.

</td></tr><tr><td>

Sales Opportunity\[sn\_lg\_contracts\_sales\_opportunity\]

</td><td>

Stores all opportunities associated with sales accounts.The data is pulled from the Microsoft Dynamics CRM system using a scheduled import set job.

</td></tr><tr><td>

Sales Opportunity Import Set\[sn\_lg\_contracts\_sales\_opportunity\_import\_set\]

</td><td>

Staging table for sales opportunity records pulled from the Microsoft Dynamics CRM system.

</td></tr><tr><td>

Sales Representative\[sn\_lg\_contracts\_sales\_representative\]

</td><td>

Stores sales representatives received from the CRM system.The data is pulled from the Microsoft Dynamics CRM system using a scheduled import set job that runs daily.

</td></tr><tr><td>

Sales Representative Import Set\[sn\_lg\_contracts\_sales\_representative\_import\_set\]

</td><td>

Staging table for sales representative records pulled from the Microsoft Dynamics CRM system.

</td></tr><tr><td>

Signer \[sn\_lg\_contracts\_signer\]

</td><td>

Stores information of internal and external signatories.

</td></tr><tr><td>

Signer Config \[sn\_lg\_contracts\_signer\_config\]

</td><td>

Stores the mapping between an internal signatory and the participant field of a document template.

</td></tr><tr><td>

Signer Task\[sn\_lg\_contracts\_signer\_task\]

</td><td>

Stores all signatory information, including the order of signatories to sign the contract document and current signature status a request.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Simple Contracts reference](legal-simple-contracts-reference.md)

