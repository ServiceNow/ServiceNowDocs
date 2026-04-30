---
title: Create a CI relation rollup
description: A CI relation rollup allows you to sum, count, max, min, or mean a relationship type. You can create CI relation rollups.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [CI relationships in the CMDB, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI relation rollup

A CI relation rollup allows you to sum, count, max, min, or mean a relationship type. You can create CI relation rollups.

## Before you begin

Role required: ecmdb\_admin

## About this task

CI relation rollup can be useful for tracking and for receiving notifications. For example:

-   In a sum roll up, add up fields from multiple CIs and display the result on another CI to which they are related. So, if you have four configuration items in a rack that are all consuming power, create a CI relation rollup to add all the power usage together and display the result in one field on the rack CI form.
-   If a certain level of power consumption in a rack is exceeded, send a notification.
-   With a rack that has 10 slots, send a notification when 9 slots are filled.

CI relation rollups use the **cmdb synch event** business rule on the \[cmdb\_ci\] table. Although this business rule is active by default, you must modify the rule slightly before it will run.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Relationships** &gt; **CI Relation Rollups**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |CI Relationship Type|Select a relationship type from the list to use with the rollup. For example, **Members::Member** of contains the parent descriptor **Members** and the child descriptor **Member of**.|
    |Type|Select the type of rollup from the drop-down list: COUNT, MAX, MEAN, MIN, or SUM.|
    |Parent field|The target field on which the operation will be done.|
    |Child field|The input to the equation type. The Parent field is affected by the selections in the child field.|
    |Rollup class|The classes that can use the relationship. For example, you can specify that the relationship only applies to racks.|

4.  To run the **cmdb synch event** business rule, navigate to **Business Rules**.

5.  Use the search box to find the \[cmdb synch event\] table.

6.  Click the **cmdb synch event** business rule to go to the **Business Rule** page.

7.  Select the **Update**, **Delete**, and **Query** check boxes.

    Additionally, if you wish CI relation rollups to recalculate when there is a change to a relationship, use a similar procedure to select the **Active** check box on the **cmdb\_rel\_ci synch event** business rule.


**Parent Topic:**[CI relationships in the CMDB](../concept/c_CIRelationships.md)

**Related topics**  


[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](t_AddANewSuggestedRelationship.md)

[Relationship governance rules](../concept/relationship-governance.md)

[CI relations formatter](../concept/c_CIRelationsFormatterNG.md)

[CI relationship editor](../concept/c_RelationshipEditor.md)

[Relation qualifier](../concept/c_RelationQualifier.md)

[CI relationship security](../concept/c_CIRelationshipSecurity.md)

[CI relationships in the CMDB](../concept/c_CIRelationships.md)

