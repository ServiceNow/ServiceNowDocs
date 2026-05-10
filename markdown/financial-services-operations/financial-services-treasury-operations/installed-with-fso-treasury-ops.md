---
title: Components installed with Financial Services Treasury Operations
description: Several types of components are installed with installation of the Financial Services Treasury Operations application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they are not already installed.
locale: en-US
release: australia
product: Financial Services Treasury Operations
classification: financial-services-treasury-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Treasury Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Treasury Operations

Several types of components are installed with installation of the Financial Services Treasury Operations application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they are not already installed.

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
|Financial Services Operations Core|Stores the customer data that is needed to make treasury service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Document Processor|Enables the management of document services tasks that are used in Financial Services Treasury Operations operations workflows. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-playbooks.md).|
|CSM Contributor User|Enables middle office teams to create cases for customer requests. For more information, see [CSM Contributor User](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/config-contributor-user.md).|

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Treasury admin\[sn\_bom\_treasury.admin\]

</td><td>

Application-specific system administrator role for treasury operations that can:-   Grant treasury operations roles
-   Delete treasury service cases and tasks
-   Configure the treasury operations application
-   Create and modify treasury service definitions
-   Read, write, and create access to treasury data

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_treasury.agent
-   sn\_bom\_treasury.manager

</td></tr><tr><td>

Treasury agent\[sn\_bom\_treasury.agent\]

</td><td>

-   Create treasury service cases and enter case data
-   View the overall status of cases
-   Work on treasury service cases and tasks

</td><td>

-   sn\_bom.service\_viewer
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.rdc\_service\_viewer
-   sn\_bom.b2b\_checking\_account\_viewer
-   sn\_bom.b2b\_saving\_account\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom\_document.b2b\_collector
-   sn\_bom.wire\_transfer\_service\_viewer

</td></tr><tr><td>

Treasury manager\[sn\_bom\_treasury.manager\]

</td><td>

-   View the Performance Analytics reports in the Treasury dashboard
-   Use Process Mining projects for treasury operations processes

</td><td>

-   sn\_bom\_treasury.agent
-   pa\_viewer

</td></tr><tr><td>

Treasury contributor\[sn\_bom\_treasury.contributor\]

</td><td>

-   Submit service requests for treasury product activation or modification
-   View the status of treasury service cases and document services tasks
-   Work on treasury cases till the Initiate and Review stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.service\_definition\_read
-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.rdc\_service\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.b2b\_checking\_account\_viewer
-   sn\_bom.b2b\_saving\_account\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor
-   sn\_bom\_document.b2b\_collector
-   sn\_bom.wire\_transfer\_service\_viewer

</td></tr><tr><td>

Treasury agent connector\[sn\_bom\_treasury.agent\_connector\]

</td><td>

-   Submit treasury service requests
-   Work on treasury cases and tasks to fulfil requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.service\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.rdc\_service\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.b2b\_checking\_account\_viewer
-   sn\_bom.agent
-   sn\_bom.b2b\_saving\_account\_viewer
-   sn\_bom\_document.b2b\_collector
-   sn\_bom.wire\_transfer\_service\_viewer

</td></tr><tr><td>

Treasury viewer\[sn\_bom\_treasury.viewer\]

</td><td>

Has read-only access to all treasury service cases and related data

</td><td>

-   sn\_bom.service\_viewer
-   sn\_bom.service\_definition\_read

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Treasury Base\[sn\_bom\_treasury\_base\]

</td><td>

Treasury Service Case table extends the Treasury Base table. Treasury Base table extends the Financial Services Base \[sn\_bom\_case\] table.

</td></tr><tr><td>

Treasury Service Case\[sn\_bom\_treasury\_service\]

</td><td>

Stores all treasury cases. This table extends the Treasury Base \[sn\_bom\_treasury\_base\] table.

</td></tr><tr><td>

RDC Service Case\[sn\_bom\_treasury\_rdc\_service\]

</td><td>

Stores all treasury cases related to RDC service requests. This table extends the Treasury Service Case \[sn\_bom\_treasury\_service\] table.

</td></tr><tr><td>

Wire Service Case\[sn\_bom\_treasury\_wire\_service\]

</td><td>

Stores all treasury cases related to wire service requests. This table extends the Treasury Service Case \[sn\_bom\_treasury\_service\] table.

</td></tr><tr><td>

Treasury Service Financial Account\[sn\_bom\_treasury\_service\_financial\_account\]

</td><td>

Intermediate table that stores all financial account level configurations for requested treasury services. This table has mapping between the Financial Account \[sn\_bom\_financial\_account\] and Treasury Service Case \[sn\_bom\_treasury\_service\] tables.

</td></tr><tr><td>

Treasury Service User\[sn\_bom\_treasury\_service\_user\]

</td><td>

Intermediate table that stores all user \(contact\) level configurations for requested treasury services. This table has mapping between the Contact \[customer\_contact\] and Treasury Service Case \[sn\_bom\_treasury\_service\] tables.

</td></tr><tr><td>

Treasury Task\[sn\_bom\_treasury\_task\]

</td><td>

Stores all treasury tasks for all treasury cases. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Treasury Operations reference](../concept/fso-treasury-operations-reference.md)

