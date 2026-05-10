---
title: Components installed with Legal Request Management
description: Several types of components are installed with activation of the Legal Request Management application, including tables and user roles.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Reference, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Request Management

Several types of components are installed with activation of the Legal Request Management application, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles

**Note:** Some roles in the **Contains roles** column are available with installation of the respective Legal Service Delivery application. For example, roles with an sn\_lg\_matter prefix are added when you install the Legal Matter Management application.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Legal Administrator\[sn\_lg\_ops.legal\_admin\]

</td><td>

Provides administrative access to all legal apps and the underlying data.

</td><td>

-   sn\_lg\_coi.coi\_admin
-   sn\_lg\_contracts.contracts\_admin
-   sn\_lg\_forensics.forensics\_admin
-   sn\_lg\_investigate.admin
-   sn\_lg\_ops.request\_admin
-   sn\_lg\_pa.pa\_admin
-   sn\_lg\_matter.matter\_admin
-   sn\_lg\_stock\_cp.stock\_config
-   sn\_lg\_cf\_workspace.admin
-   sn\_lg\_awa.admin
-   sn\_lg\_pi.admin

</td></tr><tr><td>

Legal Assignment Rules Administrator\[sn\_lg\_ops.legal\_assignment\_rules\_admin\]

</td><td>

Provides administrative access to the Assignment Rules module in legal apps.

</td><td>

-   assignment\_rule\_admin
-   sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Legal Catalog Administrator\[sn\_lg\_ops.legal\_catalog\_admin\]

</td><td>

Provides administrative access to the Catalog administration module in legal apps.

</td><td>

-   catalog\_admin
-   catalog\_editor
-   sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Legal Configurator\[sn\_lg\_ops.legal\_config\]

</td><td>

Provides access to configure data such as practice area, category, and legal matter templates. It doesn’t provide access to the transactional data of legal requests and matters.

</td><td>

-   sn\_lg\_contracts.contracts\_config
-   sn\_lg\_forensics.forensics\_config
-   sn\_lg\_investigate.config
-   sn\_lg\_ops.request\_config
-   sn\_lg\_matter.matter\_config

</td></tr><tr><td>

Legal Event Administrator\[sn\_lg\_ops.legal\_event\_manager\]

</td><td>

Provides read-only access to the Events module in legal apps.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Legal Fulfiller\[sn\_lg\_ops.legal\_fulfiller\]

</td><td>

Provides fulfiller access for working on assigned legal requests and matters.

</td><td>

-   awa\_agent
-   sn\_lg\_contracts.contracts\_fulfiller
-   sn\_lg\_forensics.forensics\_fulfiller
-   sn\_lg\_investigate.fulfiller
-   sn\_lg\_ops.request\_fulfiller
-   sn\_lg\_matter.matter\_fulfiller

</td></tr><tr><td>

Legal Manager\[sn\_lg\_ops.legal\_manager\]

</td><td>

Provides access to all transactional data of legal requests and matters and permission to assign owners for requests and matters.

</td><td>

-   sn\_lg\_coi.coi\_fulfiller
-   sn\_lg\_ops.legal\_event\_manager
-   sn\_lg\_ops.request\_manager
-   sn\_lg\_matter.matter\_manager

</td></tr><tr><td>

Legal Notification Administrator\[sn\_lg\_ops.legal\_notification\_admin\]

</td><td>

Provides administrative access to the Notifications module in legal apps to configure email notifications. **Important:** To add or modify notifications, you need the admin role.

</td><td>

-   sn\_lg\_ops.legal\_user
-   usage\_admin

</td></tr><tr><td>

Legal Report Publisher\[sn\_lg\_ops.legal\_report\_publisher\]

</td><td>

Provides restricted access to legal request and legal matter data for publishing the related reports.

</td><td>

-   report\_publisher
-   sn\_lg\_ops.legal\_report\_viewer
-   sn\_lg\_ops.legal\_user
-   pa\_power\_user
-   pa\_data\_collector

</td></tr><tr><td>

Legal Report Viewer\[sn\_lg\_ops.legal\_report\_viewer\]

</td><td>

Provides restricted access to users to view reports for legal requests and matters on the Legal Operations and Legal Executive dashboards.

</td><td>

-   report\_user
-   sn\_lg\_ops.legal\_user
-   pa\_viewer

</td></tr><tr><td>

Legal Request Fulfiller\[sn\_lg\_ops.request\_fulfiller\]

</td><td>

Provides fulfiller access for working on assigned requests.

</td><td>

-   approver\_user
-   canvas\_user
-   task\_editor
-   sn\_templated\_snip.template\_snippet\_reader
-   sn\_lg\_ops.legal\_report\_viewer
-   workspace\_user
-   sn\_uxc\_gen\_ai.platform\_ai\_field\_predictor
-   email\_composer
-   sn\_lg\_ops.legal\_user
-   email\_composer
-   sn\_uxc\_gen\_ai.platform\_ai\_record\_mgmt
-   knowledge
-   sn\_lg\_ops.legal\_sla\_read
-   awa\_agent
-   sn\_lg\_cf\_workspace.legal\_workspace\_user

 **Important:** sn\_lg\_cf\_workspace.legal\_workspace\_user inherits workspace\_user that provides access to the Next Experience Workspace.

</td></tr><tr><td>

Legal SLA Read\[sn\_lg\_ops.legal\_sla\_read\]

</td><td>

Provides access to view SLAs created on requests.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Legal User\[sn\_lg\_ops.legal\_user\]

</td><td>

Provides access to submit legal requests and track their progress. Can work on assigned tasks related to matters.

</td><td>

sn\_interview\_temp.reader

</td></tr><tr><td>

Request Administrator\[sn\_lg\_ops.request\_admin\]

</td><td>

Provides administrative access to the Legal Request module with full access to data.

</td><td>

-   sn\_lg\_ops.legal\_catalog\_admin
-   sn\_lg\_ops.request\_config
-   sn\_lg\_ops.request\_manager

</td></tr><tr><td>

Request Configurator\[sn\_lg\_ops.request\_config\]

</td><td>

Provides access to configure data such as a practice area and category, and manage record producers through Catalog Builder. It does not provide access to the transactional data of legal requests.

</td><td>

-   catalog\_builder\_editor
-   catalog\_editor
-   connection\_admin
-   email\_client\_quick\_message\_author
-   sla\_manager
-   sn\_lg\_ops.legal\_assignment\_rules\_admin
-   sn\_lg\_ops.legal\_notification\_admin
-   sn\_lg\_ops.legal\_user
-   sn\_lg\_stock\_cp.stock\_config
-   sn\_templated\_snip.template\_snippet\_writer

</td></tr><tr><td>

Request Manager\[sn\_lg\_ops.request\_manager\]

</td><td>

Provides access to all transactional data of legal requests and permission to assign requests.

</td><td>

sn\_lg\_ops.request\_fulfiller

</td></tr></tbody>
</table>## Scheduled jobs

**Note:** The following scheduled jobs are applicable when the **Enable External Storage for attachment** option is added to an intake form. For more information, see [Add an intake form to a practice area](../task/associate-categories-practice-area.md).

|Scheduled job|Description|
|-------------|-----------|
|Process External Storage Permissions​|The job selects and executes all scheduled permission records on documents for legal requests stored in external storage.|
|Retry External Document Failure|The job is executed on demand by the administrator to retry failed document uploads to external storage.​|

## Tables

**Note:** In addition to the following tables, tables specific to practice areas are installed with Legal Request Management. For more information, see [Practice area tables for legal requests](legal-request-pa-tables.md).

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog Defaults\[sn\_lg\_ops\_catalog\_default\]

</td><td>

Stores service catalog defaults such as any declarations content or templates for specific legal request.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Category\[sn\_lg\_ops\_category\]

</td><td>

Stores intake forms of a practice area. These intake forms categorize legal requests into relevant groups.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

CRM\[sn\_lg\_ops\_integration\_crm\]

</td><td>

Stores configuration details for Customer Relationship Management \(CRM\) apps such as Microsoft Dynamics CRM. Extends the Legal Integration table.

</td></tr><tr><td>

Document\(sn\_lg\_ops\_external\_document\)

</td><td>

Stores the details of the documents for legal requests stored in an external storage.This table is applicable when the **Enable External Storage for attachment** option is added to an intake form. For more information, see [Add an intake form to a practice area](../task/associate-categories-practice-area.md).

</td></tr><tr><td>

Electronic Signature\[sn\_lg\_ops\_integration\_esignature\]

</td><td>

Stores configuration details for external electronic signature such as Adobe Acrobat Sign or Docusign.This table extends the Legal Integration table.

</td></tr><tr><td>

External Apps Configuration \(Deprecated\) \[sn\_lg\_ops\_external\_configuration\]

</td><td>

The table has been deprecated. Use the Legal Integration, Electronic Signature, and External Storage tables instead.

</td></tr><tr><td>

External Storage\[sn\_lg\_ops\_integration\_external\_storage\]

</td><td>

Stores configuration details for external storage systems such as Google Drive or Box.Extends the Legal Integration table.

</td></tr><tr><td>

Integration Provider\[sn\_lg\_ops\_integration\_provider\]

</td><td>

Stores the details of external apps used by Legal Service Delivery applications.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Legal Disposition\[sn\_lg\_ops\_legal\_disposition\]

</td><td>

Stores disposition details for legal requests such as patents, contracts, and lobbying.

</td></tr><tr><td>

Legal Event Schedule Entry\[sn\_lg\_ops\_schedule\_span\]

</td><td>

Stores scheduled items such as meetings or appointments for a legal department user.

</td></tr><tr><td>

Legal External Folder\(sn\_lg\_ops\_external\_folder\)​

</td><td>

Stores URLs and details of folders created in the external storage system to save documents for each legal request.This table is applicable when the **Enable External Storage for attachment** option is added to an intake form. For more information, see [Add an intake form to a practice area](../task/associate-categories-practice-area.md).

</td></tr><tr><td>

Legal Integration\[sn\_lg\_ops\_integration\_core\]

</td><td>

Stores configuration details of external applications for storage and electronic signatures.

</td></tr><tr><td>

Legal Profile\[sn\_lg\_ops\_legal\_profile\]

</td><td>

Stores all legal data associated with an employee​ such as active legal holds, full legal name, and citizenship information that can be used for specific Legal Practice Applications \(LPAs\).

</td></tr><tr><td>

Legal Profile Association\[sn\_lg\_ops\_legal\_profile\_association\]

</td><td>

Stores the association between a legal profile and legal requests or legal matters.

</td></tr><tr><td>

Legal Request\[sn\_lg\_ops\_request\]

</td><td>

Stores legal requests submitted by a user.

</td></tr><tr><td>

Legal Schedules\[sn\_lg\_ops\_schedule\]

</td><td>

Stores the schedule for a legal department user.

</td></tr><tr><td>

Legal Types\[sn\_lg\_ops\_legal\_type\_mapping\]

</td><td>

Stores the legal request type: Legal request, matter, or matter task.

</td></tr><tr><td>

Milestones\[sn\_lg\_ops\_milestone\_schedule\_span\]

</td><td>

Stores the milestones related to a legal request.

</td></tr><tr><td>

Option\[sn\_lg\_ops\_option\]

</td><td>

Stores the predefined options to change the default behavior of legal requests and legal matters.​ You can set these options while configuring the intake form of a practice area. For more information, see [Add an intake form to a practice area](../task/associate-categories-practice-area.md).Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Practice Area\[sn\_lg\_ops\_practice\_area\]

</td><td>

Stores practice area details.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Practice Area Lead\[sn\_lg\_ops\_m2m\_practice\_area\_lead\]

</td><td>

Stores practice area leads for different practice areas.

</td></tr><tr><td>

Subcategory\[sn\_lg\_ops\_subcategory\]

</td><td>

Stores the subcategories associated with an intake form of a practice area.Extends the Application File \[sys\_metadata\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Request Management reference](legal-request-management-reference.md)

