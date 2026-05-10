---
title: Components installed with Financial Services Business Deposit Operations
description: Several types of components are installed with installation of the Financial Services Business Deposit Operations application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they aren’t already installed.
locale: en-US
release: australia
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Business Deposit Operations

Several types of components are installed with installation of the Financial Services Business Deposit Operations application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they aren’t already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

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
|Financial Services Operations Core|Stores the customer data that is needed to make deposit service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Document Processor|Enables management of document services tasks that are used in Financial Services Business Deposit Operations workflows. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-playbooks.md).|
|CSM Contributor User|Enables middle office teams to create cases for customer requests. For more information, see [CSM Contributor User](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/config-contributor-user.md) [Configure Contributor Users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/config-contributor-user.md).|

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Deposit admin\[sn\_bom\_deposit\_b2b.admin\]

</td><td>

Application-specific system administrator role for deposit operations that can:-   Grant deposit operations roles
-   Delete deposit service cases and tasks
-   Configure the deposit operations application
-   Create and modify deposit service definitions
-   Read, write, and create access to deposit data

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_deposit\_b2b.agent
-   sn\_bom\_deposit\_b2b.manager

</td></tr><tr><td>

Deposit agent\[sn\_bom\_deposit\_b2b.agent\]

</td><td>

-   Create deposit service cases and enter case data
-   View the overall status of cases
-   Work on deposit service cases and tasks

</td><td>

-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom\_document.b2b\_collector
-   sn\_bom.deposit\_account\_viewer

</td></tr><tr><td>

Deposit contributor\[sn\_bom\_deposit\_b2b.contributor\]

</td><td>

-   Create deposit service cases and enter case data
-   View the overall status of cases
-   Work on deposit service cases and tasks until the Initiate and review stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Deposit agent connector\[sn\_bom\_deposit\_b2b.agent\_connector\]

</td><td>

-   Create deposit service cases and enter case data
-   View the overall status of cases
-   Work on deposit service cases and tasks to fulfill requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Deposit manager\[sn\_bom\_deposit\_b2b.manager\]

</td><td>

-   View the Performance Analytics reports in the deposit operations dashboard
-   Use Process Mining projects for deposit operations processes

</td><td>

sn\_bom\_deposit\_b2b.agent

</td></tr><tr><td>

Deposit viewer\[sn\_bom\_deposit\_b2b.viewer\]

</td><td>

Has read-only access to all deposit service cases and related data

</td><td>

-   sn\_bom.service\_definition\_read
-   sn\_bom.account\_data\_viewer
-   sn\_bom.deposit\_account\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deposit Base\[sn\_bom\_deposit\_b2b\_base\]

</td><td>

Business Deposit Service Case table extends the Deposit Base table. Deposit Base table extends the Financial Services Base \[sn\_bom\_case\] table.

</td></tr><tr><td>

Deposit Operating Instruction\[sn\_bom\_deposit\_b2b\_operating\_instruction\]

</td><td>

Stores all operating instructions for all business deposit cases.

</td></tr><tr><td>

Business Deposit Service Case\[sn\_bom\_deposit\_b2b\_service\]

</td><td>

Stores all business deposit cases. This table extends the Deposit Base \[sn\_bom\_deposit\_b2b\_base\] table.

</td></tr><tr><td>

Business Deposit Task\[sn\_bom\_deposit\_b2b\_task\]

</td><td>

Stores all deposit tasks for all business deposit cases. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Deposit Operations reference](../concept/fso-deposit-ops-reference.md)

