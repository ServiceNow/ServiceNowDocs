---
title: Add a suggested relationship
description: Add a suggested relationship for a class. The list of suggested relationships for a class is available when you create a new relationship for a CI of that class.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/t\_AddANewSuggestedRelationship.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Add a suggested relationship

Add a suggested relationship for a class. The list of suggested relationships for a class is available when you create a new relationship for a CI of that class.

## Before you begin

Role required:

-   sn\_cmdb\_editor or itil: Read access
-   sn\_cmdb\_admin or itil\_admin: Create, update, or delete suggested relationships

.

## Procedure

1.  Use the CI Class Manager \(Role required: sn\_cmdb\_admin or itil\_admin\):

    1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

    2.  Select **Hierarchy** to expand the CI Classes list. Then select the class to add a suggested relationship to.

    3.  In the class navigation bar, click **Suggested Relationships**.

    4.  Click **New**.

    5.  In the Add Suggested Relationship dialog box, select a **Relationship** and a **Target Class** for the relationship. **This Class** and the **Target Class** become parent or child in the suggested relationship, based on your selection of the **Relationship**.

    6.  Click **Save**.

2.  Or, navigate to **All** &gt; **Configuration** &gt; **Relationships** &gt; **Suggested Relationships** \(Role required: sn\_cmdb\_admin or admin\):

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

**Parent Topic:**[CI relationships in the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CIRelationships.md)

**Related topics**  


[Suggested class relationships]()

[Relationship governance rules]()

[CI relations formatter]()

[CI relationship editor]()

[Relation qualifier]()

[CI relationship security]()

[Create a CI relation rollup]()

