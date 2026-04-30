---
title: Components installed with Individual Life Claims
description: Several types of components are installed with the activation of the Individual Life Claims application.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Individual Life Claims reference, Individual Life Claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Individual Life Claims

Several types of components are installed with the activation of the Individual Life Claims application.

## Plugins installed

|Plugin|Description|
|------|-----------|
|Customer Service \[com.sn\_customerservice\]|Enables the extension of tables from the Customer Service Management application into the Financial Services Operations applications.|

## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the customer data that is needed to make policy service requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Playbooks for Customer Service Management|Provides a way to visualize business process workflows in a simple, task-oriented view, enabling consistent responses to commonly encountered situations. For more information, see[Playbook capabilities](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).|

## Roles installed

<table id="table_um5_yjb_qbc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Individual Life Claims Admin \[sn\_ins\_claim\_indl.admin\]

</td><td>

This role gives access to all Individual Life claim operations data, plus admin privileges.

</td><td>

-   sn\_ins\_siu.viewer
-   sn\_bom.service\_definition\_admin
-   decision\_table\_admin
-   sn\_ins\_claim\_indl.dbn\_adjuster
-   sn\_ins\_claim\_indl.manager
-   sn\_doc\_processor.admin

</td></tr><tr><td>

Individual Life Claims Death Benefit Adjuster \[sn\_ins\_claim\_indl.dbn\_adjuster\]

</td><td>

This role gives access to all Individual Life Death Benefit Claim adjuster operations data.

</td><td>

-   sn\_bom.viewer
-   sn\_sla\_definition\_read
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.case\_contributor\_viewer
-   sn\_doc\_processor.agent
-   sn\_bom.adjuster
-   sn\_bom.agent
-   sn\_bom.indiv\_life\_policy\_viewer

</td></tr><tr><td>

Individual Life Claims Death Benefit Viewer \[sn\_ins\_claim\_indl.dbn\_viewer\]

</td><td>

This role gives read access to all Individual Life Death Benefit Claim operations data.

</td><td>

-   sn\_bom.service\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.indiv\_life\_policy\_viewer

</td></tr><tr><td>

Individual Life Claims First-Notice-of-Loss \(FNOL\) Representative \[sn\_ins\_claim\_indl.fnol\_representative\]

</td><td>

This role gives access to request an Individual Life Claim.

</td><td>

-   sn\_bom.indiv\_life\_policy\_viewer
-   sn\_sla\_definition\_read
-   sn\_customerservice.account\_contributor
-   sn\_bom.fnol\_representative
-   sn\_bom.customer\_data\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.case\_contributor\_viewer
-   sn\_customerservice.consumer\_contributor

</td></tr><tr><td>

Individual Life Claims Manager \[sn\_ins\_claim\_indl.manager\]

</td><td>

This role is for managing reports and dashboards, as well as approving reserves and payments above the adjuster limit.

</td><td>

sn\_ins\_claim\_indl.dbn\_adjuster

</td></tr></tbody>
</table>## Tables installed

|Table|Description|
|-----|-----------|
|Individual Death Claim \[sn\_ins\_claim\_indl\_death\_case\]|Stores information about the individual death claims. This table extends the Claim Base \[sn\_bom\_claim\_case\] table.|
|Related Death Policy Claim \[sn\_ins\_claim\_indl\_rel\_death\_case\]|Stores information about the related death claims from each policy that is attached to the customer.|
|Individual Death Claim Task \[sn\_ins\_claim\_indl\_death\_task\]|Stores information about all the individual death claims tasks for all the individual life claims. This table extends the Financial Task \[sn\_bom\_task\] table.|

**Parent Topic:**[Individual Life Claims reference](../concept/individual-life-claims-reference.md)

