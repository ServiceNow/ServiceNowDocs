---
title: Components installed with Financial Services Complaint Management
description: Several types of components are installed with installation of the Financial Services Complaint Management application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they are not already installed.
locale: en-US
release: australia
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Complaint Management, Common applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Complaint Management

Several types of components are installed with installation of the Financial Services Complaint Management application, including tables, user roles, and scheduled jobs. The application also installs related plugins and store applications if they are not already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

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
|Financial Services Operations Core|Stores the customer data that is needed to make complaint service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).|

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Complaint admin\[sn\_bom\_compl.admin\]

</td><td>

Application-specific system administrator role for complaint management that can:-   Grant complaint management roles
-   Delete complaint service cases and tasks
-   Configure the complaint management application
-   Create and modify complaint service definitions
-   Has read, write, and create access to complaint data

 **Note:** The sn\_bom.admin role contains the sn\_bom\_compl.admin role when the Financial Services Complaint Management application is installed.

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_compl.agent
-   sn\_bom\_compl.quality\_agent

</td></tr><tr><td>

Complaint agent\[sn\_bom\_compl.agent\]

</td><td>

-   View the overall status of complaint service cases
-   Work on complaint service cases and tasks

</td><td>

-   sn\_bom\_compl.viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

Complaint contributor\[sn\_bom\_compl.contributor\]

</td><td>

-   Submit complaint service requests
-   Work on complaint cases and tasks for accounts managed by them until the Initiate and Review stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom\_compl.viewer
-   sn\_sla\_definition\_read
-   sn\_bom.b2c\_contributor
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor

</td></tr><tr><td>

Complaint agent connector\[sn\_bom\_compl.agent\_connector\]

</td><td>

-   Submit complaint service requests
-   Work on complaint cases and tasks to resolve complaints for accounts managed by them.

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom\_compl.viewer
-   sn\_sla\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.agent

</td></tr><tr><td>

Quality agent\[sn\_bom\_compl.quality\_agent\]

</td><td>

-   View the overall status of quality control tasks for complaint service cases
-   Work on quality control tasks for complaint service cases

</td><td>

-   sn\_bom\_compl.viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

Complaint viewer\[sn\_bom\_compl.viewer\]

</td><td>

View complaint service cases and related data

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.ins\_policy\_viewer
-   sn\_bom.line\_of\_credit\_viewer
-   sn\_bom.deposit\_account\_viewer

</td></tr><tr><td>

Complaint manager\[sn\_bom\_compl.manager\]

</td><td>

-   View the Complaint dashboard
-   Use Process Mining for complaint management processes

</td><td>

-   sn\_bom\_compl.agent
-   pa\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Complaint Base\[sn\_bom\_compl\_base\]

</td><td>

Complaint Case table extends the Complaint Base table. Complaint Base table extends the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Complaint Case\[sn\_bom\_compl\_service\]

</td><td>

Stores all complaint cases. This table extends the Complaint Base \[sn\_bom\_compl\_base\] table.

</td></tr><tr><td>

Complaint Service Task\[sn\_bom\_compl\_task\]

</td><td>

Stores all complaint tasks. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Quality Control Task\[sn\_bom\_compl\_qc\_task\]

</td><td>

Stores all quality control tasks for complaint cases. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Regulation Category\[sn\_bom\_compl\_regulation\_category\]

</td><td>

Stores all regulation categories.

</td></tr><tr><td>

Regulation Subcategory\[sn\_bom\_compl\_regulation\_subcategory\]

</td><td>

Stores all regulation subcategories associated with regulation categories.

</td></tr></tbody>
</table>