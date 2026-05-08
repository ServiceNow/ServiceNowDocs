---
title: Activate Employee Relations
description: You can activate Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.Several types of components are installed with activation of the Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\] plugin, including tables, and user roles.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Employee Relations, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Activate Employee Relations

You can activate Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\] enables you to create and manage employee relations cases.

<table id="table_bz2_txh_zkb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Human Resources Scoped App: Core \[com.sn\_hr\_core\]

</td><td>

Enables you to standardize the documentation, interaction, and fulfillment of employee inquiries and requests.**Note:** Employee relations require activation of this plugin, but is a separate scope.

</td></tr><tr><td>

Human Resources Scoped app: Workspace \[com.sn\_hr\_agent\_workspace\]

</td><td>

A single-pane view that tier 1 agents use to respond to all task types, view the full context of an issue, and get relevant recommendations to resolve issues.**Note:** This plugin is optional for ER.

</td></tr><tr><td>

Evidence Management \[com.sn\_evidence\_management\]

</td><td>

Enables you to collect, categorize, retain, and secure evidence for use in ER cases. Evidence that requires gathering and reviewing artifacts for an investigation.This plugin activates when the Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\] is activated, but is reusable with other products and applications.

</td></tr><tr><td>

Interview Templates \[com.sn\_interview\_templates\]

</td><td>

Enables you to create reusable interview question templates. Having interview templates provides consistent and efficient interviews for Employee Relation interviews.This plugin also controls read, write, and access to interviews.

 **Note:** This plugin is optional for ER.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## Components installed with HR Service Delivery Employee Relations

Several types of components are installed with activation of the Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\] plugin, including tables, and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

Demo data is available for this feature.

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR ER administrator\[sn\_hr\_er.admin\]

</td><td>

Can access and configure HR Service Delivery Employee Relations.

</td><td>

-   ER case writer \[sn\_hr\_er.case\_writer\]
-   ER configuration manager \[sn\_hr\_er.config\_manager\]

</td></tr><tr><td>

HR ER case reader\[sn\_hr\_er.case\_reader\]

</td><td>

Can access and view HR ER cases.

</td><td>

HR case reader \[sn\_hr\_core.case\_reader\]

</td></tr><tr><td>

HR ER case writer\[sn\_hr\_er.case\_writer\]

</td><td>

Can access, create, and edit HR ER cases.

</td><td>

-   HR case reader \[sn\_hr\_core.case\_reader\]
-   HR case writer \[sn\_hr\_core.case\_writer\]

</td></tr><tr><td>

HR ER confidential\[sn\_hr\_er.confidential\]

</td><td>

Can access locked HR ER cases when locking configuration is activated.

</td><td>

-   HR basic \[sn\_hr\_core.basic\]
-   HR case writer \[sn\_hr\_core.case\_writer\]

</td></tr><tr><td>

HR ER configuration manager\[sn\_hr\_er.config\_manager\]

</td><td>

Can access, setup, and edit HR ER configuration.

</td><td>

None

</td></tr></tbody>
</table>**Note:** Impersonating another user with an ER role is not supported.

### Tables installed

<table id="table_nwz_p1y_2lb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allegation\[sn\_hr\_er\_allegation\]

</td><td>

Contains information about an allegation type and subtype.**Note:** A non-metadata table.

</td></tr><tr><td>

Allegation Subtype\[sn\_hr\_er\_allegation\_subtype\]

</td><td>

Metadata table that provides 59 records to the base system. Allegation subtypes further define an allegation. For example:-   Allegation type = Discrimination
-   Allegation subtypes: Age, disability, Race, and so on.

</td></tr><tr><td>

Allegation Type\[sn\_hr\_er\_allegation\_type\]

</td><td>

Metadata table that provides base system records. Examples are:-   Customer Mistreatment
-   Discrimination
-   Drugs and Alcohol
-   Fraud and Theft
-   Harassment
-   Interpersonal Conflict
-   Misconduct
-   Retaliation
-   Wage and Scheduling Issue
-   Workplace Violence

</td></tr><tr><td>

Associated Allegation\[sn\_hr\_er\_m2m\_allegation\_party\]

</td><td>

Contains information that associates an allegation to subject of allegations.**Note:** A non-metadata table.

</td></tr><tr><td>

Case Restriction Configuration\[sn\_hr\_er\_case\_restriction\]

</td><td>

Extends the COE Security Policy \[sn\_hr\_core\_coe\_security\_policy\] table.

</td></tr><tr><td>

Corrective Action\[sn\_hr\_er\_corrective\_action\]

</td><td>

Contains information on corrective actions associated with an ER case.**Note:** A non-metadata table.

</td></tr><tr><td>

Employee Relations Case\[sn\_hr\_er\_case\]

</td><td>

Extends the HR case \[sn\_hr\_case\] table.**Note:** A non-metadata table.

</td></tr><tr><td>

Interview\[sn\_hr\_er\_interview\]

</td><td>

Contains information related to ER interviews.**Note:** A non-metadata table.

</td></tr><tr><td>

Interview Question Template\[sn\_interview\_question\_template\]

</td><td>

Contains information related to the interview question template.Available when the Interview Templates \[com.sn\_interview\_templates\] plugin is activated.

</td></tr><tr><td>

Involved Party\[sn\_hr\_er\_involved\_party\]

</td><td>

Contains information on involved parties related to the ER case.**Note:** A non-metadata table.

</td></tr></tbody>
</table>