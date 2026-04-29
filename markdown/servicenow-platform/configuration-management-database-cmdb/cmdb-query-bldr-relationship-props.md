---
title: Configure the relationships to query on
description: Configure the type of relationships that you want to query for in CMDB Query Builder. For example, configure which CI on the canvas is the parent and which is the child in the relationship or the level of relationships to query on.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the relationships to query on

Configure the type of relationships that you want to query for in CMDB Query Builder. For example, configure which CI on the canvas is the parent and which is the child in the relationship or the level of relationships to query on.

## Before you begin

Role required: cmdb\_query\_builder\_read

## About this task

When you connect CI classes on the canvas, the CMDB Query Builder displays the Connection Properties in the right-side bar, where you can configure the properties of the relationship to query on. For Service Mapping queries, you can also configure whether to query for related or unrelated CIs.

**Note:** Newly added relationships between CI classes might take up to 30 minutes to appear in the relationship list.

## Procedure

1.  While adding CIs to the canvas, select a connection box on a CI and then select the connection box on another CI that you want to create a relationship with.

2.  Configure the relationship properties in the Connection Properties side-bar.

<table id="table_jcm_3sr_p1c"><thead><tr><th>

Section

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Relationship Direction

</td><td>

**Parent**

 **Child**

</td><td>

Set the relationship direction. Which CI class is the parent and which CI class is the child in the relationship.

</td></tr><tr><td>

Relationship Levels

</td><td>

**Level**

</td><td>

Query only on first-level relationship or also on second-level relationships.

</td></tr><tr><td>

Relationship Types and Related Items

</td><td>

**No Relationships**

</td><td>

Select to query for CIs which have no relationships to the set class.

</td></tr><tr><td>

Relationship Types and Related Items

</td><td>

Select **Add Relationship Types**

</td><td>

Query for CIs and descending classes with specific relationship types.

</td></tr><tr><td>

Relationship Types and Related Items

</td><td>

Select **Add a Related Item**

</td><td>

Query on related CIs using a field that the parent and ancestor parent CI classes use to reference the child CI class.

</td></tr></tbody>
</table>3.  Select **Save**.


**Related topics**  


[CMDB groups](../concept/cmdb-groups.md#)

