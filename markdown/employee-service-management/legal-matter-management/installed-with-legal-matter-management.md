---
title: Components installed with Legal Matter Management
description: Several types of components are installed with installation of the Legal Matter Management application, including tables, and user roles.
locale: en-US
release: xanadu
product: Legal Matter Management
classification: legal-matter-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legal Matter Management reference, Legal Matter Management, Legal Service Delivery, Employee Service Management]
---

# Components installed with Legal Matter Management

Several types of components are installed with installation of the Legal Matter Management application, including tables, and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles

<table id="table_legal_matter_roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Matter Administrator\[sn\_lg\_matter.matter\_admin\]

</td><td>

Provides the administrative access to legal matters and the underlying data.

</td><td>

-   sn\_lg\_matter.matter\_config
-   sn\_lg\_matter.matter\_manager

</td></tr><tr><td>

Matter Configurator\[sn\_lg\_matter.matter\_config\]

</td><td>

Provides access to configure data such as practice areas, intake forms, matter templates, and manage record producers through Catalog Builder. It does not provide access to transactional data of legal requests and legal matters.

</td><td>

-   catalog\_builder\_editor
-   catalog\_editor
-   connection\_admin
-   email\_client\_quick\_message\_author
-   flow\_designer
-   flow\_designer\_scripting
-   sla\_manager
-   sn\_interview\_temp.writer
-   sn\_lg\_matter.matter\_config\_read
-   sn\_templated\_snip.template\_snippet\_writer

</td></tr><tr><td>

Matter Configurator Read-only\[sn\_lg\_matter.matter\_config\_read\]

</td><td>

Provides read-only access to legal apps configuration data such as practice areas and matter templates.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Matter Fulfiller\[sn\_lg\_matter.matter\_fulfiller\]

</td><td>

Provides the fulfiller access for working on assigned matters.

</td><td>

-   approver\_user
-   email\_composer
-   knowledge
-   sn\_interview\_temp.reader
-   sn\_lg\_matter.matter\_config\_read
-   sn\_lg\_ops.legal\_report\_viewer
-   sn\_lg\_ops.legal\_sla\_read
-   sn\_templated\_snip.template\_snippet\_reader
-   task\_editor
-   workspace\_user
-   awa\_agent

 **Important:** sn\_lg\_cf\_workspace.legal\_workspace\_user inherits workspace\_user that provides access to the Next Experience Workspace.

</td></tr><tr><td>

Matter Manager\[sn\_lg\_matter.matter\_manager\]

</td><td>

Provides access to all transactional data of matters and permission to assign matters.

</td><td>

-   sn\_interview\_temp.writer
-   sn\_lg\_matter.matter\_fulfiller

</td></tr></tbody>
</table>## Tables

**Note:** In addition to the following tables, tables specific to practice areas are installed with Legal Matter Management. For more information, see [Practice area tables for legal matters](legal-matter-pa-tables.md).

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Artifact Content Type\[sn\_lg\_matter\_artifact\_content\_type\]

</td><td>

Stores the content type used for categorizing matter artifacts.

</td></tr><tr><td>

Approver Group\[sn\_lg\_matter\_m2m\_approver\_group\]

</td><td>

Stores user groups who can approve legal matter templates.

</td></tr><tr><td>

External Storage\[sn\_lg\_matter\_artifact\_external\_storage\]

</td><td>

Stores links of external systems such as Microsoft OneDrive or Microsoft SharePoint where matter documents can be stored.

</td></tr><tr><td>

Legal Artifact\[sn\_lg\_matter\_artifact\]

</td><td>

Stores the artifact details collected for a matter.

</td></tr><tr><td>

Legal Matter\[sn\_lg\_matter\_matter\]

</td><td>

Stores legal matters.

</td></tr><tr><td>

Legal Matter Core\[sn\_lg\_matter\_core\]

</td><td>

Stores the core details of a matter.

</td></tr><tr><td>

Legal Matter Phase\[sn\_lg\_matter\_phase\]

</td><td>

Stores the phases of a matter.

</td></tr><tr><td>

Legal Matter Task\[sn\_lg\_matter\_task\]

</td><td>

Stores the tasks associated to a phase or a matter.

</td></tr><tr><td>

Matter Task Artifact\[sn\_lg\_matter\_m2m\_matter\_task\_artifact\]

</td><td>

Stores the details of the relationship between an artifact and a matter task.

</td></tr><tr><td>

Matter Task Template\[sn\_lg\_matter\_template\_task\]

</td><td>

Stores the tasks defined in a matter template.

</td></tr><tr><td>

Matter Template\[sn\_lg\_matter\_template\]

</td><td>

Stores the matter template that defines the default values for a matter. Creating a matter from the matter template populates predefined values in the matter.

</td></tr><tr><td>

Request - Matter m2m\[sn\_lg\_matter\_m2m\_request\_matter\]

</td><td>

Stores the details of the relationship between a request and a matter.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Matter Management reference](legal-matter-management-reference.md)

