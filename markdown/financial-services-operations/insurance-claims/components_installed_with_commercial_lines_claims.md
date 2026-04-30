---
title: Components installed with Commercial Lines Claims
description: Several types of components are installed with activation of the sn\_ins\_claim\_cml plugin, including plugins, tables, and user roles.
locale: en-US
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Commercial Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Commercial Lines Claims

Several types of components are installed with activation of the sn\_ins\_claim\_cml plugin, including plugins, tables, and user roles.

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

</th></tr></thead><tbody><tr><td colspan="3">

Commercial Lines Claims

</td></tr><tr><td>

Commercial Lines Claims admin\[sn\_ins\_claim\_cml.admin\]

</td><td>

-   Grant Commercial Lines Claims roles
-   Delete Commercial Lines Claims cases and tasks
-   Configure Commercial Lines Claims application
-   Create and modify Commercial Lines Claims service definitions
-   Has read, write, and create access to Commercial Lines Claims policy or case data

</td><td>

-   decision\_table\_admin
-   sn\_bom.service\_definition\_admin
-   sn\_ins\_claim\_cml.admin
-   sn\_ins\_claim\_cml.auto\_processor
-   sn\_ins\_siu.viewer
-   sn\_doc\_processor.admin
-   sn\_ins\_claim\_cml.auto\_adjuster

</td></tr><tr><td>

Commercial Lines Claims manager\[sn\_ins\_claim\_cml.manager\]

</td><td>

-   View the Commercial Lines Claims dashboard
-   Use Process Mining for Commercial Lines Claims processes

</td><td>

-   sn\_ins\_claim\_cml.auto\_adjuster
-   sn\_ins\_claim\_cml.auto\_processor
-   pa\_viewer

</td></tr><tr><td>

Commercial Lines Claims adjuster\[sn\_ins\_claim\_cml.auto\_adjuster\]

</td><td>

-   Evaluates the commercial auto claim details based on assigned adjuster tasks, and settles claims
-   Views the status of commercial auto claim cases
-   Creates and edits ad-hoc tasks

</td><td>

-   sn\_customerservice.case\_contributor\_viewer
-   sn\_doc\_processor.agent
-   sn\_bom.adjuster
-   sn\_ins\_claim\_cml.auto\_processor
-   sn\_sla\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.ca\_ins\_policy\_viewer
-   sn\_customerservice.csm\_workspace\_user

</td></tr><tr><td>

Commercial Lines Claims processor\[sn\_ins\_claim\_cml.auto\_processor\]

</td><td>

-   Submits commercial auto claim details, and creates and edits ad-hoc tasks
-   Views the status of commercial auto claim cases
-   Closes a claim
-   Records interactions

</td><td>

-   sn\_customerservice.case\_contributor\_viewer
-   sn\_ins\_claim.payment\_reader
-   sn\_ins\_claim.reserve\_reader
-   sn\_ins\_claim.fraud\_score\_reader
-   sn\_ins\_claim.property\_writer
-   sn\_bom.ca\_ins\_policy\_viewer
-   sn\_ins\_claim.coverage\_writer
-   sn\_ins\_claim.summary\_page\_read
-   sn\_bom.b2b\_agent
-   sn\_ins\_claim.participant\_writer
-   sn\_ins\_claim.policy\_snapshot\_reader
-   sn\_ins\_claim.profile\_writer
-   sn\_ins\_claim.injury\_writer

</td></tr><tr><td>

Commercial Lines Claims viewer\[sn\_ins\_claim\_cml.auto\_viewer\]

</td><td>

View commercial auto claim cases and related data.

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.account\_data\_viewer
-   sn\_bom.ca\_ins\_policy\_viewer

</td></tr><tr><td>

Commercial Lines Claims FNOL representative\[sn\_ins\_claim\_cml.fnol\_representative\]

</td><td>

Create and track commercial claim cases for policies managed by them.

</td><td>

-   sn\_customerservice.case\_contributor\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom.account\_data\_viewer
-   sn\_customerservice.consumer\_contributor
-   sn\_bom.ca\_ins\_policy\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.account\_contributor
-   sn\_bom.fnol\_representative

</td></tr><tr><td colspan="3">

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

</th></tr></thead><tbody><tr><td colspan="2">

Commercial Lines Claims

</td></tr><tr><td>

Commercial Auto Claim Case

 \[sn\_ins\_claim\_cml\_auto\_service\]

</td><td>

Stores information about commercial claim cases. This table extends the Commercial Claim Base \[sn\_ins\_claim\_cml\_base\] table.

</td></tr><tr><td>

Commercial Auto Claim Task \[sn\_ins\_claim\_cml\_auto\_task\]

</td><td>

Stores information about all commercial claims tasks for all commercial claims cases.

</td></tr><tr><td>

Commercial Auto Claim Adjuster Task \[sn\_ins\_claim\_cml\_auto\_adj\_task\]

</td><td>

Stores information about tasks related to the adjuster persona for commercial claims.

</td></tr><tr><td>

Commercial Claim Basesn\_ins\_claim\_cml\_base

</td><td>

Extends the Claim Base \[sn\_bom\_claim\_base\] table.

</td></tr><tr><td>

Property Incident\[sn\_ins\_claim\_cml\_auto\_incident\]

</td><td>

Stores information about property incident details for commercial claims cases. This table extends the Claim Incident \[sn\_ins\_claim\_property\] table from Insurance Claims Core.

</td></tr><tr><td colspan="2">

Insurance Special Investigations

</td></tr><tr><td>

SIU Tasksn\_ins\_siu\_task

</td><td>

Stores information about tasks related to the Special Investigation Unit department for all claims auto cases.

</td></tr></tbody>
</table>