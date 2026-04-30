---
title: Components installed with Supplier Lifecycle Operations
description: Several types of components are installed with activation of Supplier Lifecycle Operations, including tables and user roles.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Components installed with Supplier Lifecycle Operations

Several types of components are installed with activation of Supplier Lifecycle Operations, including tables and user roles.

The user roles and tables, even though installed along with Supplier Lifecycle Operations, reside in the Supplier Common Architecture application. For more information, see [Supplier Common Architecture](../concept/supplier-common.md).

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

**Note:** Users with the Supplier Manager \[sn\_slm.manager\], Supplier Fulfiller \[sn\_slm.fulfiller\], and Supplier Owner \[sn\_slm.owner\] roles cannot access the Supplier Collaboration Portal.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Supplier Administrator\[sn\_slm.admin\]

</td><td>

The supplier admin can create, view, update, and delete all the suppliers, cases, and tasks.

</td><td>

-   decision\_table\_admin
-   sn\_shop.shopper
-   awa\_admin
-   sn\_vdr\_risk\_asmt.vendor\_assessor
-   sn\_fin.supplier\_payment\_info\_write
-   sn\_slm.manager
-   sn\_kpi.admin

</td></tr><tr><td>

Supplier Fulfiller\[sn\_slm.fulfiller\]

</td><td>

Users with this role can do the following: -   Create tasks
-   View suppliers related to assigned cases or tasks
-   View assigned cases and tasks, or tasks that are created by them
-   Update assigned cases and tasks, or tasks that are created by them

</td><td>

-   task\_editor
-   template\_read\_global
-   sn\_shop.shopper
-   workspace\_user
-   vendor\_reader
-   canvas\_user
-   sn\_fin.finance\_user
-   awa\_agent
-   survey\_reader
-   sn\_fin.procurement\_user
-   email\_composer

</td></tr><tr><td>

Supplier Owner\[sn\_slm.owner\]

</td><td>

The supplier owner can do everything the supplier fulfiller can do, plus users with this role can:-   Create suppliers using the playbook
-   Create cases and tasks for suppliers they own
-   View the suppliers they own
-   View cases and tasks for the suppliers they own
-   Update the suppliers they own
-   Update the cases and tasks that are created by them or assigned to them

**Note:** The Supplier Owner \[sn\_slm.owner\] role can create, manage, and edit records for only the suppliers that they own.

</td><td>

-   personalize\_responses
-   workspace\_user
-   canvas\_user
-   sn\_slm.fulfiller
-   sn\_fin.finance\_user
-   sn\_fin.procurement\_user
-   sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

</td></tr><tr><td>

Supplier Manager\[sn\_slm.manager\]

</td><td>

The supplier manager can do everything the supplier owner can do, plus users with this role can: -   Create suppliers using the playbook
-   Create cases and tasks
-   View all the suppliers, cases, and tasks
-   Update the suppliers they manage and also other suppliers
-   Update the cases and tasks that they create or that are assigned to them

</td><td>

-   sn\_slm.owner
-   dm\_user\_criteria\_read

</td></tr><tr><td>

Supplier Agentsn\_slm.agent

</td><td>

The supplier agent can do everything the supplier fulfiller can do, plus users with this role can:-   Create cases and tasks
-   View all the suppliers, cases, and tasks
-   Update all the tasks and assigned cases

</td><td>

sn\_slm.fulfiller

</td></tr><tr><td>

Supplier Contact\[sn\_slm.contact\]

</td><td>

A user with this role can do the following:-   Submit requests using the supplier catalog from the Supplier Collaboration Portal
-   Complete assigned tasks using the Supplier Collaboration Portal

**Note:** A contact can be a primary contact or secondary contact. A primary contact is a user that has the Primary contact column set to **true** on the Vendor Contacts page.

</td><td>

-   sn\_fin.supplier\_payment\_info\_read
-   snc\_external

</td></tr><tr><td>

KPI Administrator\[sn\_kpi.admin\]

</td><td>

The KPI admin can define, manage, and analyze KPIs​.

</td><td>

sn\_kpi.user**Note:** Added after the Xanadu December 2024 upgrade.

</td></tr><tr><td>

KPI User\[sn\_kpi.user\]

</td><td>

The KPI user can only read all the records in KPI Framework.

</td><td>

**Note:** Added after the Xanadu December 2024 upgrade.

</td></tr><tr><td>

KPI Data Owner\[sn\_kpi.data\_owner\]

</td><td>

The KPI data owner can access only specific tables and fields which are necessary to collect data for KPIs from an internal user.​

</td><td>

**Note:** Added after the Xanadu December 2024 upgrade.

</td></tr></tbody>
</table>## Tables installed

**Note:** The Supplier Payment Information \[sn\_fin\_supplier\_payment\] table, which stores the bank account records of the suppliers, is installed with the Finance Common Architecture \(com.sn\_fin\) application.

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Supplier Case \[sn\_slm\_case\]

</td><td>

Stores the supplier case records. Extends the Service Case \[sn\_spend\_sdc\_service\_request\] table.

</td></tr><tr><td>

Supplier Product Code \[sn\_slm\_code\_m2m\_supplier\]

</td><td>

Stores the relationships between suppliers in the Supplier \[sn\_fin\_supplier\] table and product codes in the Product Code \[sn\_supplier\_product\_code\] table.

</td></tr><tr><td>

Supplier Email Domain \[sn\_slm\_email\_domain\]

</td><td>

Stores the email domains of the suppliers.

</td></tr><tr><td>

Supplier Location \[sn\_slm\_m2m\_location\]

</td><td>

Stores the relationships between suppliers stored in the Supplier \[sn\_fin\_supplier\] table and locations stored in the Location \[cmn\_location\] table.

</td></tr><tr><td>

Supplier Contact \[sn\_slm\_supplier\_m2m\_contact\]

</td><td>

Stores the supplier contact and supplier records. It is used for the M2M mapping of one contact with many suppliers.

</td></tr><tr><td>

Product Code \[sn\_slm\_product\_code\]

</td><td>

Stores the product and service records with universal product codes \(UPC\). These records do not have any relation to the supplier.

</td></tr><tr><td>

Supplier Task \[sn\_slm\_task\]

</td><td>

Stores the tasks of the suppliers. Extends the Service Task \(sn\_spend\_sdc\_service\_task\) table.

</td></tr><tr><td>

Supplier Document Configuration \[sn\_slm\_document\_config\]

</td><td>

Stores the supplier document configurations. Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Supplier Document Type \[sn\_slm\_document\_type\]

</td><td>

Stores the supplier document types. Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Supplier Document References \[sn\_slm\_document\_references\]

</td><td>

Stores the supplier document references. Extends the Document References \[ds\_document\_references\] table.

</td></tr><tr><td>

Organization Tax Details

 \[sn\_fin\_org\_tax\_detail\]

</td><td>

Stores the tax registration details of the supplier.**Note:** This table has been added in the Finance Common Architecture \(com.sn\_fin\) plugin.

</td></tr></tbody>
</table>**Parent Topic:**[Install Supplier Lifecycle Operations](../task/install-supp-mgmt.md)

