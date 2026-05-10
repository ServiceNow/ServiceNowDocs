---
title: Components installed with Intelligent Servicing for Fraud
description: Several types of components are installed with the activation of the Intelligent Servicing for Fraud \(sn\_bom\_fraud\) plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Intelligent Servicing for Fraud
classification: intelligent-servicing-for-fraud
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Intelligent Servicing for Fraud, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Intelligent Servicing for Fraud

Several types of components are installed with the activation of the Intelligent Servicing for Fraud \(sn\_bom\_fraud\) plugin, including tables, user roles, and scheduled jobs.

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
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-playbooks.md).|

## Roles installed

<table id="table_qzw_m3l_4pb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_bom\_fraud.admin

</td><td>

creates, reads, updates, and deletes \(CRUD\) operations on fraud cases.

</td><td>

-   decision\_table\_admin
-   sn\_bom.service\_definition\_admin
-   sn\_bom\_fraud.agent
-   sn\_doc\_processor.admin

</td></tr><tr><td>

sn\_bom\_fraud.agent

</td><td>

Accesses and views fraud data as a fraud agent.

</td><td>

-   sn\_doc\_processor.agent
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

sn\_bom\_fraud.viewer

</td><td>

Grants access to view fraud cases.

</td><td>

-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr><tr><td>

sn\_bom\_fraud.manager

</td><td>

Approves or rejects fraud cases.

</td><td>

sn\_bom\_fraud.agent

</td></tr><tr><td>

sn\_bom\_fraud.contributor

</td><td>

Creates a fraud case on behalf of the customer.

</td><td>

-   sn\_bom.account\_viewer
-   sn\_doc\_processor.collector
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_sla\_definition\_read
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr><tr><td>

sn\_bom\_fraud.agent\_connector

</td><td>

Creates, views, and edits fraud cases and works with consumers to resolve cases.

</td><td>

-   sn\_doc\_processor.agent
-   sn\_sla\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fraud Case \[sn\_bom\_fraud\_case\]

</td><td>

Stores all alerts that are flagged by the external fraud detection systems. This table is also used to log and investigate fraud cases that are reported by customers or by external entities such as the law enforcement agency or regulators in a country.

 The Fraud Case table extends the Financial Services Base table. Services Base table extends the Case **\[sn\_customerservice\_case\]** table.

</td></tr><tr><td>

Fraud Task \[sn\_bom\_fraud\_task\]

</td><td>

Stores all fraud tasks. This table is used by fraud agents as a subtask to complete their fraud cases. For example, write off and report to risk and compliance.The Fraud Task table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Fraud Transaction \[sn\_bom\_fraud\_transaction\]

</td><td>

Stores the fraud transaction information and outcome of business rules that are triggered at various stages in the life cycle of the case.

</td></tr></tbody>
</table>## Decision tables installed

|Name|Description|
|----|-----------|
|Card fraud policy rules|Rules to decide whether investigation is allowed for a transaction and to determine its associated customer liability.|
|Card fraud risk evaluation rules|Rules to determine risk associated with a transaction.|
|Fraud investigation routing rules|Rules to decide whether to route case to Fraud investigator group or not.|

