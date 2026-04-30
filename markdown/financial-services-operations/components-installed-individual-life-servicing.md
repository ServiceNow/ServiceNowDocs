---
title: Components installed with Individual Life Servicing
description: Several types of components are installed with activation of the Individual Life Servicing plugin, including tables and user roles.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Individual Life Servicing reference, Setting up Individual Life Servicing, Individual Life Servicing, Life Insurance Servicing, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Individual Life Servicing

Several types of components are installed with activation of the Individual Life Servicing plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Plugins installed

<table><thead><tr><th>

Plugin name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service\[com.sn\_customerservice\]

</td><td>

Enables the extension of tables from the Customer Service Management application into the Financial Services Operations applications.

</td></tr><tr><td>

Individual Life Insurance Underwriting Operations\[sn\_ins\_indiv\_uw\]

</td><td>

Enables insurance carriers to route service requests to underwriters based on their existing underwriting guidelines and rules. Underwriters can collaborate with distribution and servicing teams though a workflow.

</td></tr></tbody>
</table>## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the customer data that is needed to make policy service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Individual Life Insurance Underwriting Operations|Enables management of individual policy underwriting services tasks that are used in insurance policy service workflows. For more information, see [Components installed with Individual Life Underwriting](components-installed-with-individual-life-underwriting.md).|
|Document Processor|Enables management of document services tasks that are used in insurance policy service cases. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).|
|CSM Contributor User|Enables middle office teams to create cases for customer requests. For more information, see [CSM Contributor User](https://www.servicenow.com/docs/access?context=config-contributor-user&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) [Configure Contributor Users](https://www.servicenow.com/docs/access?context=config-contributor-user&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).|

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Individual policy admin

 \[sn\_ins\_indiv\_life.admin\]

</td><td>

-   Grant individual insurance servicing roles
-   Delete individual policy cases and tasks
-   Configure Individual Life Servicing application
-   Create and modify individual policy service definitions
-   Has read, write, and create access to individual policy data

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_ins\_indiv\_life.line\_writer
-   sn\_ins\_indiv\_life.processor
-   sn\_ins\_indiv\_life.processor\_connector

</td></tr><tr><td>

Individual life manager

\[sn\_ins\_indiv\_life.manager\]

</td><td>

-   View the Performance Analytics reports in the Individual Life Servicing dashboard
-   Use Process Mining projects for insurance operations processes

</td><td>

-   sn\_ins\_indiv\_life.processor
-   sn\_ins\_indiv\_life.processor\_connector

</td></tr><tr><td>

Individual policy processor \[sn\_ins\_indiv\_life.processor\]

</td><td>

-   Submit individual insurance policy service requests
-   View the status of individual insurance policy cases, underwriting tasks, and document services tasks
-   Record interactions

</td><td>

-   sn\_ins\_indiv\_life.line\_writer
-   sn\_doc\_processor.agent
-   sn\_ins\_indiv\_uw.viewer
-   sn\_bom.indiv\_life\_policy\_viewer
-   sn\_bom.indiv\_disab\_policy\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

Individual policy processor connector\[sn\_ins\_indiv\_life.processor\_connector\]

</td><td>

-   Access and view the status of individual life and disability policy cases, underwriting tasks, and document services tasks for customer accounts managed by them.
-   Create, update, and close cases and tasks for customer accounts managed by them
-   Record interactions

</td><td>

-   sn\_ins\_indiv\_life.viewer
-   sn\_doc\_processor.agent
-   sn\_ins\_indiv\_life.line\_writer
-   sn\_sla\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_ins\_indiv\_uw.viewer
-   sn\_bom.viewer
-   sn\_bom.indiv\_life\_policy\_viewer
-   sn\_bom.indiv\_disab\_policy\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.agent
-   sn\_ins\_indiv\_life.line\_viewer

</td></tr><tr><td>

Individual policy contributor\[sn\_ins\_indiv\_life.contributor\]

</td><td>

Create and track policy service cases for accounts managed by them.**Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.service\_viewer
-   sn\_ins\_indiv\_life.lineinfo\_writer
-   sn\_sla\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_ins\_indiv\_uw.viewer
-   sn\_bom.b2c\_contributor
-   sn\_bom.indiv\_life\_policy\_viewer
-   sn\_bom.indiv\_disab\_policy\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor
-   sn\_ins\_indiv\_life.line\_viewer
-   sn\_bom.ins\_policy\_viewer

</td></tr><tr><td>

Individual policy viewer\[sn\_ins\_indiv\_life.viewer\]

</td><td>

View individual insurance policy cases and related data

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.indiv\_life\_policy\_viewer
-   sn\_ins\_indiv\_life.info\_viewer
-   sn\_bom.ins\_policy\_viewer

</td></tr></tbody>
</table>## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Individual Life Policy Base

 \[sn\_ins\_indiv\_life\_base\]

</td><td>

Policy Base table extends the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Individual Life Policy Case\[sn\_ins\_indiv\_life\_service\]

</td><td>

Policy Service Case table extends the Policy Base table. Stores all policy service cases for consumer services for the Individual Life Servicing

</td></tr><tr><td>

Individual Life Policy Task\[sn\_ins\_indiv\_life\_task\]

</td><td>

This table extends the Financial Task \[sn\_bom\_task\] table. Stores all policy tasks for policy services for the Individual Life Servicing

</td></tr><tr><td>

Policy Coverage Line\[sn\_ins\_indiv\_life\_coverage\_line\]

</td><td>

This is an Info table which stores the changes to coverages of policy services for the Individual Life Servicing

</td></tr></tbody>
</table>