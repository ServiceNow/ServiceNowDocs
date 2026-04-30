---
title: Add a suggested relationship
description: Add a suggested relationship for a class. The list of suggested relationships for a class is available when you create a new relationship for a CI of that class.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Add a suggested relationship

Add a suggested relationship for a class. The list of suggested relationships for a class is available when you create a new relationship for a CI of that class.

## Before you begin

Role required: To view — itil. To create, update, or delete suggested relationships — itil\_admin.

## Procedure

1.  Use the CI Class Manager \(Role required: itil\_admin\):

    1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

    2.  Click **Hierarchy** to expand the CI Classes list. Then select the class to add a suggested relationship to.

    3.  In the class navigation bar, click **Suggested Relationships**.

    4.  Click **New**.

    5.  In the Add Suggested Relationship dialog box, select a **Relationship** and a **Target Class** for the relationship. **This Class** and the **Target Class** become parent or child in the suggested relationship, based on your selection of the **Relationship**.

    6.  Click **Save**.

2.  Or, navigate to **All** &gt; **Configuration** &gt; **Relationships** &gt; **Suggested Relationships** \(Role required: admin\):

    1.  Click **New**.

    2.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |Base class|The base class in the relationship, which depending on the relationship type, is either the parent or the child in the relationship.|
        |Relationship|Relationship type.|
        |Dependent class|The dependent class in the relationship, which depending on the relationship type, is either the parent or the child in the relationship.|


## Suggested relationship you can add

|Base Class|Relationship|Dependent/Target Class|
|----------|------------|----------------------|
|Oracle|Is Hosted On|Linux Server|
|Oracle|Is Hosted On|Solaris Server|

**Note:** The same parent class and relationship can appear more than once.

## What to do next

You may need to delete a suggested relationship, for example, to limit the choice of available relationships in the CI relationship editor. Removing a suggested relationship does not affect relationships that are created or updated by Discovery.

**Parent Topic:**[CI relationships in the CMDB](../concept/c_CIRelationships.md)

**Related topics**  


[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Relationship governance rules](../concept/relationship-governance.md)

[CI relations formatter](../concept/c_CIRelationsFormatterNG.md)

[CI relationship editor](../concept/c_RelationshipEditor.md)

[Relation qualifier](../concept/c_RelationQualifier.md)

[CI relationship security](../concept/c_CIRelationshipSecurity.md)

[Create a CI relation rollup](t_CreateACIRelationRollup.md)

