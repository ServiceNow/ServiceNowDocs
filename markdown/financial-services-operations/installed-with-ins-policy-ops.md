---
title: Components installed with Personal Lines Servicing
description: Several types of components are installed with the installation of the Financial Services Insurance Policy Operations Personal Lines Servicing store applications, including tables and user roles. The applications also install related plugins and store applications if they are not already installed.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Personal Lines Servicing, Property and Casualty Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Personal Lines Servicing

Several types of components are installed with the installation of the Financial Services Insurance Policy Operations Personal Lines Servicing store applications, including tables and user roles. The applications also install related plugins and store applications if they are not already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

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
|Financial Services Operations Core|Stores the customer data that is needed to make policy service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Personal Lines Underwriting|Enables management of personal underwriting services tasks that are used in insurance policy service cases. For more information, see [Components installed with Personal Lines Underwriting](installed-with-fso-underwriting-ops.md).|
|Document Processor|Enables the management of document services tasks that are used in insurance operations workflows. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see Playbooks for Customer Service Management.|

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Personal insurance policy admin\[sn\_ins\_policy\_b2c.admin\]

</td><td>

Application-specific system administrator role for personal insurance policy that can:-   Grant personal property and casualty insurance servicing roles
-   Delete personal policy cases and tasks
-   Configure personal Property and Casualty Insurance Servicing application
-   Create and modify personal policy service definitions
-   Has read, write, and create access to personal policy data

 **Note:** The sn\_bom.admin role contains the sn\_ins\_policy\_b2c.admin role when the Property and Casualty Insurance Servicing application is installed.

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_ins\_policy\_b2c.info\_writer
-   sn\_ins\_policy\_b2c.auto\_policy\_processor
-   sn\_ins\_policy\_b2c.homeowner\_policy\_processor

</td></tr><tr><td>

Personal insurance contributor\[sn\_ins\_policy\_b2c.contributor\]

</td><td>

Create and track policy service cases for accounts managed by them.**Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_sla\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_ins\_policy\_b2c.info\_writer
-   sn\_bom.homeowner\_ins\_policy\_viewer
-   sn\_bom.auto\_ins\_policy\_viewer
-   sn\_bom.b2c\_contributor
-   sn\_bom\_document.b2c\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_ins\_underwrite.viewer
-   sn\_bom\_document.b2c\_collector

</td></tr><tr><td>

Auto policy processor\[sn\_ins\_policy\_b2c.auto\_policy\_processor\]

</td><td>

-   Submit auto insurance policy service requests
-   View the status of auto insurance policy cases, underwriting tasks, and document services tasks
-   Record interactions

</td><td>

-   sn\_ins\_policy\_b2c.info\_writer
-   sn\_bom.auto\_ins\_policy\_viewer
-   sn\_bom\_document.b2c\_viewer
-   sn\_bom.b2c\_agent
-   sn\_ins\_underwrite.viewer

</td></tr><tr><td>

Auto insurance policy viewer\[sn\_ins\_policy\_b2c.auto\_policy\_viewer\]

</td><td>

View auto insurance policy cases and related data

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_ins\_policy\_b2c.ins\_policy\_viewer
-   sn\_ins\_policy\_b2c.info\_viewer

</td></tr><tr><td>

Homeowner policy processor\[sn\_ins\_policy\_b2c.homeowner\_policy\_processor\]

</td><td>

-   Submit homeowner insurance policy service requests
-   View the status of homeowner insurance policy cases, underwriting tasks, and document services tasks
-   Record interactions

</td><td>

-   sn\_ins\_policy\_b2c.info\_writer
-   sn\_bom.homeowner\_ins\_policy\_viewer
-   sn\_bom\_document.b2c\_viewer
-   sn\_bom.b2c\_agent
-   sn\_ins\_underwrite.viewer

</td></tr><tr><td>

Homeowner insurance policy viewer\[sn\_ins\_policy\_b2c.homeowner\_policy\_viewer\]

</td><td>

View homeowner insurance policy cases and related data

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_ins\_policy\_b2c.ins\_policy\_viewer
-   sn\_ins\_policy\_b2c.info\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy Base\[sn\_ins\_policy\_b2c\_base\]

</td><td>

Policy Service Case table extends the Policy Base table. Policy Base table extends the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Auto Policy Case\[sn\_ins\_policy\_b2c\_service\]

</td><td>

Stores all policy service cases for consumer services for all Financial Services Operations applications. This table extends the Policy Base \[sn\_ins\_policy\_b2c\_base\] table.

</td></tr><tr><td>

Auto Policy Task\[sn\_ins\_policy\_b2c\_task\]

</td><td>

Stores all policy tasks for policy services for all Financial Services Operations applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Homeowner Policy Case\[sn\_ins\_policy\_b2c\_home\_service\]

</td><td>

Homeowners case type table which holds all servicing cases for Homeowner policies. This table is extended off Policy Base table.

</td></tr><tr><td>

Homeowner Policy Task\[sn\_ins\_policy\_b2c\_home\_service\_task\]

</td><td>

This table extends the Financial Task \[sn\_bom\_task\] table. Stores all tasks related to a Homeowners case.

</td></tr><tr><td>

Insured Property Info\[sn\_ins\_policy\_b2c\_insured\_property\_info\]

</td><td>

This is an Info table which stores the changes to insured properties which can take place as part of servicing a case against a policy.

</td></tr><tr><td>

Participant Insured Property Info\[sn\_ins\_policy\_b2c\_participant\_insured\_property\_info\]

</td><td>

This is an Info table which stores the changes to a role that a participant plays on an insured property which can take place as part of servicing a case against a policy.

</td></tr><tr><td>

Policy Coverage Info\[sn\_ins\_policy\_b2c\_policy\_coverage\_info\]

</td><td>

This is an Info table which stores the changes to policy participants which can take place as part of servicing a case against a policy.

</td></tr><tr><td>

Policy Participant Info\[sn\_ins\_policy\_b2c\_policy\_participant\_info\]

</td><td>

This is an Info table which stores the changes to policy coverages which can take place as part of servicing a case against a policy.

</td></tr></tbody>
</table>**Parent Topic:**[Personal Lines Servicing reference](../concept/ins-policy-ops-reference.md)

