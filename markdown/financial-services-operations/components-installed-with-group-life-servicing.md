---
title: Components installed with Group Life Servicing
description: Several types of components are installed with activation of the Group Life Servicing plugin, including tables and user roles. The applications also install related plugins and store applications if they are not already installed.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Group Life Servicing, Life Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Group Life Servicing

Several types of components are installed with activation of the Group Life Servicing plugin, including tables and user roles. The applications also install related plugins and store applications if they are not already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

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

Group Life and Disability Underwriting

 \[sn\_ins\_group\_uw\]

</td><td>

Enables insurance carriers to route service requests to underwriters based on their existing underwriting guidelines and rules. Underwriters can collaborate with distribution and servicing teams though a workflow.

</td></tr></tbody>
</table>## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the customer data that is needed to make policy service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Group Life Underwriting|Enables management of group policy underwriting services tasks that are used in insurance policy service cases. For more information, see [Components installed with Group Life Underwriting](components-installed-group-life-underwriting.md).|
|Document Processor|Enables management of document services tasks that are used in insurance policy service workflows. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).|
|CSM Contributor User|Enables middle office teams to create cases for customer requests. For more information, see [CSM Contributor User](https://www.servicenow.com/docs/access?context=config-contributor-user&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) [Configure Contributor Users](https://www.servicenow.com/docs/access?context=config-contributor-user&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).|

## Roles installed

<table id="table_ph4_pl5_4tb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Group policy admin

 \[sn\_ins\_group\_life.admin\]

</td><td>

-   Grant group insurance servicing roles
-   Delete group policy cases and tasks
-   Configure Group Life Servicing application
-   Create and modify group policy service definitions
-   Has read, write, and create access to group policy data

</td><td>

-   decision\_table\_admin
-   sn\_bom.service\_definition\_admin
-   sn\_doc\_processor.admin
-   sn\_ins\_group\_life.processor

</td></tr><tr><td>

Group life manager

\[sn\_ins\_group\_life.manager\]

</td><td>

-   View the Performance Analytics reports in the Group Life Servicing dashboard
-   Use Process Mining projects for insurance operations processes

</td><td>

-   sn\_ins\_group\_life.processor
-   sn\_ins\_group\_life.processor\_connector

</td></tr><tr><td>

Group policy processor \[sn\_ins\_group\_life.processor\]

</td><td>

-   Submit group insurance policy service requests
-   View the status of group insurance policy cases, underwriting tasks, and document services tasks
-   Record interactions

</td><td>

-   sn\_doc\_processor.agent
-   sn\_ins\_group\_life.info\_viewer
-   sn\_ins\_group\_life.info\_writer
-   sn\_bom.group\_life\_ins\_policy\_viewer
-   sn\_bom.b2b\_agent
-   sn\_ins\_group\_uw.viewer

</td></tr><tr><td>

Group policy processor connector\[sn\_ins\_group\_life.processor\_connector\]

</td><td>

-   Access and view the status of individual life and disability policy cases, underwriting tasks, and document services tasks for customer accounts managed by them.
-   Create, update, and close cases and tasks for customer accounts managed by them
-   Record interactions

</td><td>

-   sn\_ins\_group\_life.info\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.agent
-   sn\_ins\_group\_life.info\_writer
-   sn\_bom.group\_life\_ins\_policy\_viewer
-   sn\_ins\_group\_uw.viewer

</td></tr><tr><td>

Group policy contributor\[sn\_ins\_group\_life.contributor\]

</td><td>

Create and track policy service cases for accounts managed by them.**Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_ins\_group\_life.info\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom.account\_data\_viewer
-   sn\_ins\_group\_life.info\_writer
-   sn\_bom.group\_life\_ins\_policy\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_ins\_group\_uw.viewer
-   sn\_bom.b2b\_contributor

</td></tr><tr><td>

Group policy viewer\[sn\_ins\_group\_life.viewer\]

</td><td>

View group insurance policy cases and related data

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.account\_data\_viewer
-   sn\_bom.group\_life\_ins\_policy\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_th4_pl5_4tb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group Life Policy Base

 \[sn\_ins\_group\_life\_base\]

</td><td>



</td></tr><tr><td>

Group Life Policy Case\[sn\_ins\_group\_life\_service\]

</td><td>

 

</td></tr><tr><td>

Group Life Policy Task\[sn\_ins\_group\_life\_task\]

</td><td>

 

</td></tr><tr><td>

Insured Property Info\[sn\_ins\_group\_life\_insured\_property\_info\]

</td><td>

 

</td></tr><tr><td>

Policy Coverage Info\[sn\_ins\_group\_life\_policy\_coverage\_info\]

</td><td>

 

</td></tr></tbody>
</table>