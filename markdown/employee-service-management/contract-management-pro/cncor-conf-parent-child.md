---
title: Configure field mapping for parent-child contract linking
description: Select the child contract type and configure the parent-child field mapping to inherit the mapped fields from the parent contract when linking.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Contract request linking, Configure parent-child contract linking, Configure parent-child field mapping, Contract request parent-child field mapping, Contract parent-child field mapping]
breadcrumb: [Create a contract type, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure field mapping for parent-child contract linking

Select the child contract type and configure the parent-child field mapping to inherit the mapped fields from the parent contract when linking.

## About this task

The following video walks you through the process of configuring parent-child field mapping to inherit mapped fields when linked.Video explaining how to configuring parent-child field mapping to inherit mapped fields when linked, approximately two minutes long. 

## About this task

You can configure a child contract type for a contract type and map the fields to automatically inherit values from the parent contract when linked. A contract type can have multiple child contract types and field mappings. You can map one field at a time.

The **Link and inherit fields** button on the Link contract window is available only when you configure the parent-child mapping.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Contract Types**.

2.  Select the contract type for which you want to configure a child contract type.

3.  In the Parent Child Mappings related list, select **New**.

4.  In the Parent Child Mapping form, configure the child contract type and map the fields.

    ![Parent child mapping form to configure field inheritance.](../image/cmpro-conf-parent-child-link.png "Parent child mapping configuration")

    |Field|Description|
    |-----|-----------|
    |Parent table|Table from which fields are to be copied for a child contract type.|
    |Child table|Table to which fields are copied.|
    |Map from field|Field in the parent table which is copied to a child contract type.|
    |Map to field|Field in the child table that inherits the field from the parent table.|
    |Child contract type|Child contract type for selected contract type.|

5.  Select **Submit**.

6.  In the Contract type form, select **Update**.


## Result

The parent child mapping is configured, and values from the mapped parent fields are inherited by the child contract when linked.

