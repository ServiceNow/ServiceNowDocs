---
title: Components installed with Financial Services Business Loan Operations
description: Several types of components are installed with the installation of the Financial Services Business Loan Operations application, including tables and user roles. The application also installs related plugins and store applications if they aren’t already installed.
locale: en-US
release: australia
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Business Loan Operations

Several types of components are installed with the installation of the Financial Services Business Loan Operations application, including tables and user roles. The application also installs related plugins and store applications if they aren’t already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Plugins installed

<table id="table_qdc_ksw_llb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service\[com.sn\_customerservice\]

</td><td>

Enables the extension of tables from the Customer Service Management application into the Financial Services Operations applications.

</td></tr></tbody>
</table>## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the customer data that is needed to make loan service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Financial Services Credit Operations|Enables the management of Credit service cases and tasks that are used in loan operations workflows. For more information, see [Components installed with Financial Services Credit Operations](../../fso-common/reference/installed-with-credit-assessment.md).|
|Document Processor|Enables the management of document services tasks that are used in loan operations workflows. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-playbooks.md).|

## Roles installed

These roles correspond to Business Loan Operations.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Loan admin\[sn\_bom\_loan\_b2b.admin\]

</td><td>

Application-specific system administrator role for business loans that can:-   Configure the loan operations application
-   Create and modify loan service definitions
-   Has read, write, and create access to loan data
-   Grant loan operations roles
-   Delete loan cases and tasks

 **Note:** The sn\_bom.admin role contains the sn\_bom\_loan\_b2b.admin role when the Financial Services Business Loan Operations application is installed.

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_loan\_b2b.agent
-   sn\_bom\_loan\_b2b.manager

</td></tr><tr><td>

Loan agent\[sn\_bom\_loan\_b2b.agent\]

</td><td>

-   View the overall status of loan cases
-   Work on loan cases and tasks to fulfil loan requests.

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.line\_of\_credit\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Loan contributor\[sn\_bom\_loan\_b2b.contributor\]

</td><td>

-   Submit loan service requests
-   View the status of loan service cases
-   Work on loan case and collect inbound documents for accounts managed by them till the Initiate and Review stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.b2b\_line\_of\_credit\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Loan agent connector\[sn\_bom\_loan\_b2b.agent\_connector\]

</td><td>

-   Submit loan service requests
-   Work on loan cases and tasks to fulfil loan requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.b2b\_line\_of\_credit\_viewer
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Loan manager\[sn\_bom\_loan\_b2b.manager\]

</td><td>

-   View the business loan operations dashboard
-   Use Process Mining for Business Loan Operations processes

</td><td>

-   sn\_bom\_loan\_b2b.agent
-   pa\_viewer

</td></tr><tr><td>

Loan viewer\[sn\_bom\_loan\_b2b.viewer\]

</td><td>

View loan cases and related data

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.account\_data\_viewer
-   sn\_bom.line\_of\_credit\_viewer
-   sn\_bom.deposit\_account\_viewer

</td></tr></tbody>
</table>## Tables installed

These tables correspond to Business Loan Operations.

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Loan Base\[sn\_bom\_loan\_base\]

</td><td>

Loan Service Case table extends the Loan Base table. Loan Base table extends the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Loan Service Case\[sn\_bom\_loan\_service\]

</td><td>

Stores all business loan service cases. This table extends the Loan Base \[sn\_bom\_loan\_base\] table.

</td></tr><tr><td>

Loan Task\[sn\_bom\_loan\_task\]

</td><td>

Stores all business loan tasks. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Loan Operations reference](../concept/loan-operations-reference.md)

