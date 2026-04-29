---
title: Components installed with Insurance claims
description: Several types of components are installed with the activation of the Insurance claims application.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Insurance claims

Several types of components are installed with the activation of the Insurance claims application.

## Plugins installed

|Plugin|Description|
|------|-----------|
|CSM Contributor User \[com.snc.csm\_contributor\_user\]|Enables the contributor role for the first-notice-of-loss \(FNOL\) representative, who creates the case on behalf of the customer.|

## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the customer data that is needed to make policy service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Playbooks in Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, enabling consistent responses to commonly encountered situations. For more information, see [Playbooks in Customer Service Management](https://www.servicenow.com/docs/access?context=setting-up-csm-playbooks&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).|

## Roles installed

<table id="table_icl_kz3_tcc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Admin \[sn\_ins\_gen\_claim.admin\]

</td><td>

This role gives access to all Insurance claims operations data, plus admin privileges.

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_ins\_gen\_claim.processor
-   decision\_table\_admin
-   sn\_ins\_gen\_claim.adjuster
-   sn\_ins\_gen\_claim.manager
-   sn\_doc\_processor.admin

</td></tr><tr><td>

FNOL representative \[sn\_ins\_gen\_claim.fnol\_representative\]

</td><td>

This role gives access to request Insurance claims for customers with whom a relationship exists.

</td><td>

-   sn\_customerservice.case\_contributor\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom.ct\_ins\_policy\_viewer
-   sn\_customerservice.customer\_contributor
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.pt\_ins\_policy\_viewer
-   sn\_bom.fnol\_representative
-   sn\_bom.customer\_data\_viewer
-   sn\_customerservice.account\_contributor

</td></tr><tr><td>

Adjuster \[sn\_ins\_gen\_claim.adjuster\]

</td><td>

This role gives access to all Insurance claims adjuster operations data.

</td><td>

-   sn\_bom.viewer
-   sn\_bom.ct\_ins\_policy\_viewer
-   sn\_bom.pt\_ins\_policy\_viewer
-   sn\_bom.adjuster
-   sn\_doc\_processor.agent
-   sn\_ins\_gen\_claim.processor
-   sn\_sla\_definition\_read

</td></tr><tr><td>

Manager \[sn\_ins\_gen\_claim.manager\]

</td><td>

This role is for managing reports and dashboards, as well as approving reserves and payments above the adjuster limit.

</td><td>

-   sn\_ins\_gen\_claim.processor
-   sn\_ins\_gen\_claim.adjuster

</td></tr><tr><td>

Viewer \[sn\_ins\_gen\_claim.viewer\]

</td><td>

This role gives read access to all Insurance claims claim operations data.

</td><td>

-   sn\_bom.customer\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.ref\_data\_viewer

</td></tr><tr><td>

Processor \[sn\_ins\_gen\_claim.processor\]

</td><td>

This role gives access to all Insurance claims operations data.

</td><td>

-   sn\_ins\_claim.payment\_reader
-   sn\_ins\_claim.trip\_writer
-   sn\_ins\_claim.property\_reader
-   sn\_ins\_claim.trip\_reader
-   sn\_bom.b2c\_agent
-   sn\_doc\_processor.agent
-   sn\_ins\_claim.injury\_reader
-   sn\_ins\_claim.participant\_writer
-   sn\_ins\_claim.policy\_snapshot\_reader
-   sn\_ins\_claim.injury\_writer
-   sn\_ins\_claim.baggage\_reader
-   sn\_ins\_claim.property\_writer
-   sn\_bom.ct\_ins\_policy\_viewer
-   sn\_ins\_claim.profile\_reader
-   sn\_ins\_claim.reserve\_reader
-   sn\_bom.b2b\_agent
-   sn\_bom.pt\_ins\_policy\_viewer
-   sn\_ins\_claim.baggage\_writer
-   sn\_ins\_claim.summary\_page\_read
-   sn\_ins\_claim.coverage\_reader
-   sn\_ins\_claim.incident\_item\_writer
-   sn\_ins\_claim.incident\_item\_reader
-   sn\_ins\_claim.incident\_config\_reader
-   sn\_sla\_definition\_read
-   sn\_ins\_claim.profile\_writer

</td></tr><tr><td>

Flow executor \[sn\_ins\_gen\_claim.flow\_executor\]

</td><td>

This role gives access to run all flows and subflows for Insurance claims.

</td><td>

sn\_ins\_gen\_claim.manager

</td></tr></tbody>
</table>## Tables installed

|Table|Description|
|-----|-----------|
|Claim Case \[sn\_ins\_gen\_claim\_case\]|Store information about the claim case. This table extends the Claim Base \[sn\_bom\_claim\_case\] table.|
|Claim Task \[sn\_ins\_gen\_claim\_task\]|Stores information about a claim task. This table extends the Financial Task \[sn\_bom\_task\] table.|
|Claim Adjuster Task \[sn\_ins\_gen\_claim\_adj\_task\]|Stores information about an adjuster task for a claim. This table extends the Financial Task \[sn\_bom\_task\] table.|

**Parent Topic:**[Insurance claims reference](../concept/insurance-claims-flow-reference.md)

