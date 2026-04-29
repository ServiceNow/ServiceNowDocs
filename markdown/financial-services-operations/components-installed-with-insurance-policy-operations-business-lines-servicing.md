---
title: Components installed with Commercial Lines Servicing
description: Several types of components are installed with the installation of the Financial Services Commercial Lines Servicing store application, including tables and user roles. The applications also install related plugins and store applications if they are not already installed.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Commercial Lines Servicing, Property and Casualty Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Commercial Lines Servicing

Several types of components are installed with the installation of the Financial Services Commercial Lines Servicing store application, including tables and user roles. The applications also install related plugins and store applications if they are not already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Plugins installed

<table><thead><tr><th>

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
|Financial Services Operations Core|Stores the customer data that is needed to make policy service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Commercial Lines Underwriting|Enables management of commercial underwriting services tasks that are used in insurance policy service cases. For more information, see [Components installed with Commercial Lines Underwriting](components-installed-with-insurance-commercial-underwriting-operations.md).|
|Document Processor|Enables the management of document services tasks that are used in insurance operations workflows. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).|

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Commercial insurance policy admin

\[sn\_ins\_policy\_b2b.admin\]

</td><td>

-   Grant commercial property and casualty insurance servicing roles
-   Delete commercial policy cases and tasks
-   Configure commercial Property and Casualty Insurance Servicing application
-   Create and modify commercial policy service definitions
-   Has read, write, and create access to commercial policy data

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_ins\_policy\_b2b.bop\_processor

</td></tr><tr><td>

Commercial policy processor\[sn\_ins\_policy\_b2b.bop\_processor\]

</td><td>

-   Submit commercial insurance policy service requests
-   View the status of commercial insurance policy cases, underwriting tasks, and document services tasks
-   Record interactions

</td><td>

-   sn\_ins\_policy\_b2b.info\_viewer
-   sn\_bom\_document.b2b\_viewer
-   sn\_ins\_policy\_b2b.info\_writer
-   sn\_bom.b2b\_agent
-   sn\_ins\_uw\_b2b.viewer
-   sn\_ins\_policy\_b2b.bop\_viewer
-   sn\_bom\_document.b2b\_collector
-   sn\_bom.bo\_ins\_policy\_viewer

</td></tr><tr><td>

Commercial insurance contributor\[sn\_ins\_policy\_b2b.contributor\]

</td><td>

Create and track policy service cases for accounts managed by them.**Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_ins\_policy\_b2b.info\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_ins\_policy\_b2b.info\_writer
-   sn\_bom.account\_data\_viewer
-   sn\_ins\_uw\_b2b.viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor
-   sn\_bom\_document.b2b\_collector
-   sn\_bom.bo\_ins\_policy\_viewer

</td></tr><tr><td>

Commercial insurance policy viewer\[sn\_ins\_policy\_b2b.bop\_viewer\]

</td><td>

View commercial insurance policy cases and related data

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_ins\_uw\_b2b.viewer
-   sn\_bom.bo\_ins\_policy\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy Base\[sn\_ins\_policy\_b2b\_base\]

</td><td>

Personal lines servicing base table extension of the Case \[sn\_customerservice\_case\] table. Any line of business specific case type tables can be extended off this table.

</td></tr><tr><td>

Business Owner Policy Case\[sn\_ins\_policy\_b2b\_bop\_service\]

</td><td>

BOP case type table which holds all servicing cases for Business Owner policies. This table is an extension of the Policy Base table.

</td></tr><tr><td>

Business Owner Policy Task\[sn\_ins\_policy\_b2b\_bop\_task\]

</td><td>

This table extends the Financial Task \[sn\_bom\_task\] table. Stores all tasks related to a BOP case.

</td></tr><tr><td>

Insured Property Info\[sn\_ins\_policy\_b2b\_insured\_property\_info\]

</td><td>

This is an Info table which stores the changes to insured properties which can take place as part of servicing a case against a policy.

</td></tr><tr><td>

Participant Insured Property Info \[sn\_ins\_policy\_b2b\_participant\_insured\_property\_info\]

</td><td>

This is an Info table which stores the changes to a role that a participant plays on an insured property which can take place as part of servicing a case against a policy.

</td></tr><tr><td>

Policy Participant Info\[sn\_ins\_policy\_b2b\_policy\_participant\_info\]

</td><td>

This is an Info table which stores the changes to policy participants which can take place as part of servicing a case against a policy.

</td></tr><tr><td>

Policy Coverage Info\[sn\_ins\_policy\_b2b\_policy\_coverage\_info\]

</td><td>

This is an Info table which stores the changes to policy coverages which can take place as part of servicing a case against a policy.

</td></tr></tbody>
</table>**Parent Topic:**[Commercial Lines Servicing reference](../concept/commercial-lines-servicing-reference.md)

