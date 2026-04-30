---
title: Components installed with Personal Lines Claims
description: Several types of components are installed with activation of the sn\_ins\_claim\_pers plugin, including plugins, tables, and user roles.
locale: en-US
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Personal Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Personal Lines Claims

Several types of components are installed with activation of the sn\_ins\_claim\_pers plugin, including plugins, tables, and user roles.

## Plugins installed

<table><thead><tr><th>

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
|Insurance Special Investigations|Insurance Special Investigations enables insurance carriers to route fraud investigation requests to SIU agents. Requests get routed via adjusters working on claim cases through workflows in the Personal Lines Claims application.|
|Document Processor|Enables management of document services tasks that are used in insurance policy service cases. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations. For more information, see [Playbooks for Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).|

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td colspan="3" align="center">

Personal Lines Claims

</td></tr><tr><td>

Personal Lines Claims admin\[sn\_ins\_claim\_pers.admin\]

</td><td>

-   Grant Personal Lines Claims roles
-   Delete Personal Lines Claims cases and tasks
-   Configure Personal Lines Claims application
-   Create and modify Personal Lines Claims service definitions
-   Has read, write, and create access to Personal Lines Claims policy or case data

</td><td>

-   decision\_table\_admin
-   sn\_bom.service\_definition\_admin
-   sn\_ins\_claim\_pers.manager
-   sn\_ins\_claim\_pers.auto\_processor
-   sn\_ins\_siu.viewer
-   sn\_doc\_processor.admin
-   sn\_ins\_claim\_pers.auto\_adjuster

</td></tr><tr><td>

Personal Lines Claims manager\[sn\_ins\_claim\_pers.manager\]

</td><td>

-   Views the Personal Lines Claims dashboard
-   Uses Process Mining for Personal Lines Claims processes

</td><td>

-   sn\_ins\_claim\_pers.auto\_adjuster
-   sn\_ins\_claim\_pers.auto\_processor
-   pa\_viewer

</td></tr><tr><td>

Personal Lines Claims adjuster\[sn\_ins\_claim\_pers.auto\_adjuster\]

</td><td>

-   Evaluates the personal auto claim details based on assigned adjuster tasks, and settles claims
-   Views the status of personal auto claim cases
-   Creates and edits ad-hoc tasks

</td><td>

-   sn\_customerservice.case\_contributor\_viewer
-   sn\_doc\_processor.agent
-   sn\_bom.adjuster
-   sn\_sla\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.auto\_ins\_policy\_viewer
-   sn\_ins\_claim\_pers.auto\_processor
-   sn\_customerservice.csm\_workspace\_user

</td></tr><tr><td>

Personal Lines Claims processor\[sn\_ins\_claim\_pers.auto\_processor\]

</td><td>

-   Submits personal auto claim details, and creates and edits ad-hoc tasks
-   Views the status of personal auto claim cases
-   Closes a claim
-   Records interactions

</td><td>

-   sn\_customerservice.case\_contributor\_viewer
-   sn\_ins\_claim.profile.writer
-   sn\_ins\_claim.payment\_reader
-   sn\_ins\_claim.reserve\_reader
-   sn\_ins\_claim.fraud\_score\_reader
-   sn\_ins\_claim.injury\_writer
-   sn\_ins\_claim.property\_writer
-   sn\_bom.auto\_ins\_policy\_viewer
-   sn\_ins\_claim.coverage\_writer
-   sn\_bom.b2c\_agent
-   sn\_ins\_claim.participant\_writer
-   sn\_ins\_claim.policy\_snapshot\_reader
-   sn\_ins\_claim.summary\_page\_read

</td></tr><tr><td>

Personal Lines Claims viewer\[sn\_ins\_claim\_pers.auto\_viewer\]

</td><td>

Views personal auto claim cases and related data.

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.auto\_ins\_policy\_viewer
-   sn\_ins\_claim\_pers.auto\_viewer

</td></tr><tr><td>

Personal Lines Claims FNOL representative\[sn\_ins\_claim\_pers.fnol\_representative\]

</td><td>

Create and track personal claim cases for policies managed by them.

</td><td>

-   sn\_customerservice.case\_contributor\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.auto\_ins\_policy\_viewer
-   sn\_customerservice.consumer\_contributor
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.account\_contributor
-   sn\_bom.fnol\_representative

</td></tr><tr><td colspan="3" align="center">

Insurance Special Investigations

</td></tr><tr><td>

Insurance Special Investigations admin\[sn\_ins\_siu.admin\]

</td><td>

-   Grant insurance special investigations roles
-   Delete special investigations cases and tasks
-   Configure Insurance Special Investigations application
-   Create and modify special investigations service definitions
-   Has read, write, and create access to special investigations case data

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_ins\_siu.agent

</td></tr><tr><td>

Insurance Special Investigations agent\[sn\_ins\_siu.agent\]

</td><td>

Submits evaluation on SIU tasks that are associated with a case.

</td><td>

-   sn\_ins\_claim.property\_reader
-   sn\_ins\_claim.payment\_reader
-   sn\_ins\_claim.reserve\_reader
-   sn\_ins\_claim.fraud\_score\_reader
-   sn\_ins\_claim\_cml.auto\_viewer
-   sn\_bom.b2b\_agent
-   sn\_ins\_claim.coverage\_reader
-   sn\_ins\_claim\_pers.auto\_viewer
-   sn\_bom.b2c\_agent
-   sn\_ins\_claim.participant\_reader

</td></tr><tr><td>

Insurance Special Investigations viewer\[sn\_ins\_siu.viewer\]

</td><td>

View special investigation cases and related data.

</td><td>

 

</td></tr></tbody>
</table>## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2" align="center">

Personal Lines Claims

</td></tr><tr><td>

Personal Auto Claim Case

 \[sn\_ins\_claim\_pers\_auto\_service\]

</td><td>

Stores information about personal claim cases. This table extends the Personal Claim Base \[sn\_ins\_claim\_pers\_base\] table.

</td></tr><tr><td>

Personal Auto Claim Task \[sn\_ins\_claim\_pers\_auto\_task\]

</td><td>

Stores information about all personal claims tasks for all personal claims cases.

</td></tr><tr><td>

Personal Auto Claim Adjuster Task \[sn\_ins\_claim\_pers\_auto\_adj\_task\]

</td><td>

Stores information about tasks related to the adjuster persona for personal claims.

</td></tr><tr><td>

Personal Claim Basesn\_ins\_claim\_pers\_base

</td><td>

Extends the Claim Base \[sn\_bom\_claim\_base\] table.

</td></tr><tr><td>

Property Incident\[sn\_ins\_claim\_pers\_auto\_incident\]

</td><td>

Stores information about property incident details for personal claims cases. This table extends the Claim Incident \[sn\_ins\_claim\_property\] table from Insurance Claims Core.

</td></tr><tr><td colspan="2" align="center">

Insurance Special Investigations

</td></tr><tr><td>

SIU Tasksn\_ins\_siu\_task

</td><td>

Stores information about tasks related to the Special Investigation Unit department for all claims cases.

</td></tr></tbody>
</table>