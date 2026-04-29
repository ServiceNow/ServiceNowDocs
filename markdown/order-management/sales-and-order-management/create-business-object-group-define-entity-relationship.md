---
title: Set up business objects for sales process records
description: Create the business objects necessary for sales process managers to create sales process records using these entities.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Lead-to-Cash Process Management, Order operations apps, Configure, Sales and Order Management]
---

# Set up business objects for sales process records

Create the business objects necessary for sales process managers to create sales process records using these entities.

## Before you begin

Role required: Business object writer \[sn\_bo\_core.business\_object\_writer\]

## About this task

Video showing the steps to set up business objects 

## Procedure

1.  Create business object groups.

    1.  Navigate to **All** &gt; **Business Object Core** &gt; **Business Object Group**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name for the business object group.|
        |Applies to|Workflow or process for which you're creating the business object group. This value should be Sales Process Record \[sn\_l2c\_cockpit\_sales\_process\_record\].|
        |Description|A brief description of the business object group.|

2.  Create business object types to add as members in the business object group.

    1.  Navigate to **All** &gt; **Business Object Core** &gt; **Business Object Types**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name for the business object type. For example, Opportunity.|
        |Table name|Table associated with the business object. For example, if the business object type is Opportunity, you would enter the Opportunity \[sn\_opty\_mgmt\_core\_opportunity\] table.|

    4.  Select **Submit**.

3.  Define relationships between the object types.

    Relationships define how two object types are related by the source and destination columns on the respective tables and govern the hierarchy of the records displayed on the node map. For example, if you add Opportunity Line and Quote as child entities for the business object type Opportunity, on the node map you would see the related Opportunity Line and Quote records under an Opportunity node.

    You can add more than one child entity under a parent business object type. Ensure that you avoid circular relationships.

    1.  Select the business object type you created.

    2.  On the Business Object Type page under the Business Object Relationships related list, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Source|The parent business object type for which you are creating the relationships.|
        |Destination|The child business object type that is related to the parent.|
        |Source table name|Table name of the parent business object type.|
        |Destination table name|Table name of the child business object type.|
        |Source field|\(Optional\) The column on the source table used for establishing the relationship.|
        |Destination field|\(Optional\) The column on the destination table used for establishing the relationship.|

    4.  Select **Submit**.

4.  Add business object types as members of business object group.

    1.  Navigate to **All** &gt; **Business Object Core** &gt; **Business Object Group**.

    2.  Under the Business Object Group Members related list, select **New**.

    3.  Select the business object type you want to add using the Lookup list icon ![](../../../reuse/icons/product-icons/magnifying-glass-outline-24.svg).

    4.  Select **Submit**.


## Result

Business object group and business object types are available in Business process and Business entity lists respectively in the Create new sales process record form in the CSM Configurable Workspace.

