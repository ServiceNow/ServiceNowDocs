---
title: Understanding FSO Core relationships
description: This section describes the key tables in FSO Core and their relationships. Understanding these relationships helps you manage data effectively and enhances system functionality.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations Core, Data Models, Explore, Financial Services Operations \(FSO\)]
---

# Understanding FSO Core relationships

This section describes the key tables in FSO Core and their relationships. Understanding these relationships helps you manage data effectively and enhances system functionality.

The Financial Services Operations Core application is automatically installed with any of the  Financial Services Operations applications but can also be installed independently for a basic configuration using only its data model.

The following table lists this application's dependencies:

|Name|Value|
|----|-----|
|Customer Service Management \(CSM\)|com.sn\_customerservice|
|Expanded Model and Asset Classes|com.sn\_ent|
|Install Base|com.snc.install\_base|

**Important:** Starting with the Vancouver release, the Financial Services Operations Core model tables will use child tables of Expanded Model and Asset's base Service model \[cmdb\_service\_product\_model\] to classify different service models within the Configuration Management Database \(CMDB\). For more information, see [Expanded Model and Asset Classes Store application](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)

## Financial Services Operations Core data model diagram

The following diagram shows the tables and their relationships that build the Financial Services Operations Core data model.

![Diagram illustrating the FSO Core data model.](../../fso-deposit-operations/image/FSO-Core-Data-model.png "Financial Services Operations Core table relationship")

## Using ServiceNow AI Platform, Customer Service Management \(CSM\) tables

The Financial Services Operations data model uses the following tables included within the ServiceNow AI Platform, Customer Service Management \(CSM\), and Configuration Management Database \(CMDB\) applications to store data.

<table id="table_q2y_mtg_2qb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Application

</th></tr></thead><tbody><tr><td>

Business location \[sn\_csm\_business\_location\]

</td><td>

Provides the business location records.

</td><td>

CSM

</td></tr><tr><td>

Case \[sn\_customerservice\_case\]

</td><td>

Provides the cases for patients associated with customer contact records.

</td><td>

CSM

</td></tr><tr><td>

Characteristic \[sn\_prd\_pm\_characteristic\]

</td><td>

Provides the attributes available for a product.

</td><td>

CSM

</td></tr><tr><td>

Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td><td>

Provides the options for attributes available for a product.

</td><td>

CSM

</td></tr><tr><td>

Consumer \[csm\_consumer\]

</td><td>

Provides patient records associated with consumer records.

</td><td>

CSM

</td></tr><tr><td>

Consumer profile \[sn\_csm\_consumer\_profile\]

</td><td>

Provides multiple consumer profiles.

</td><td>

CSM

</td></tr><tr><td>

Household Member \[csm\_household\_member\]

</td><td>

Provides records of the patient members who have been added to a household.

</td><td>

CSM

</td></tr><tr><td>

Location \[cmn\_location\]

</td><td>

Provides addresses associated with a patient.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Product Specification \[sn\_prd\_pm\_specification\]

</td><td>

Defines, at a functional level, a product a service provider sells to the customer.

</td><td>

CSM

</td></tr><tr><td>

Sold product \[sn\_install\_base\_sold\_product\]

</td><td>

Provides the product purchased by a patient as a customer and references the Product Model \[cmdb\_model\] table or Service Model \[cmdb\_service\_product\_model\] table for a customer \(customer account or consumer\).

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Specification \[sn\_prd\_pm\_specification\]

</td><td>

Provides the base table for specifications included in the industry vertical applications.

</td><td>

CSM

</td></tr><tr><td>

Specification Characteristic \[sn\_prd\_pm\_specification\_characteristic\]

</td><td>

Provides the characteristics for product, service, and resource specifications.

</td><td>

CSM

</td></tr><tr><td>

Task \[task\]

</td><td>

Provides a series of standard fields used on each of the tables that extend it.

</td><td>

ServiceNow AI Platform

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations Core](financial-services-operations-core-data-model.md)

