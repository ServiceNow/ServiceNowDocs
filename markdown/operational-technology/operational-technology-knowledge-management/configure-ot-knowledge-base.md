---
title: Create an OT knowledge base
description: Create an Operational Technology \(OT\) knowledge base to provide a self-service platform for OT knowledge users to store, share, and manage content that is related to OT incidents.
locale: en-US
release: zurich
product: Operational Technology Knowledge Management
classification: operational-technology-knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Knowledge Management, Operational Technology]
---

# Create an OT knowledge base

Create an Operational Technology \(OT\) knowledge base to provide a self-service platform for OT knowledge users to store, share, and manage content that is related to OT incidents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.

2.  Select **New**.

3.  On the knowledge base form, fill in the fields.

    For a description of the field values, see [Knowledge base form](../reference/knowledge-base-form-fields.md).

4.  Right click the form header and select **Save**.

5.  In the related list section, view or configure the items in the following table that are related to the OT knowledge base.

<table id="table_gxq_xyr_bzb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge

</td><td>

List of knowledge articles that are stored in this knowledge base.

</td></tr><tr><td>

Can Read

</td><td>

List of user criteria that grants read access and enables a user who matches the criteria to read articles in the OT knowledge base.

</td></tr><tr><td>

Can Contribute

</td><td>

List of user criteria that grants contributor access and enables users who match the criteria to create and modify the articles in the OT knowledge base.

</td></tr><tr><td>

Article Templates

</td><td>

If you’ve activated the Knowledge Management Advanced \(com.snc.knowledge\_advanced\) plugin, the Article Templates related list is displayed. If article templates are in the related list, the articles in that knowledge base can only be created by using one of the article templates listed.

If the Article Templates related list is empty, articles can be created by using any article template.

Map article templates to the knowledge base by selecting **Edit**.

**Note:** Admins, knowledge admins, and knowledge managers can edit the article templates for the knowledge base.

</td></tr><tr><td>

Knowledge categories

</td><td>

List of knowledge categories that are associated with the OT knowledge base. **Note:** If the category is marked as inactive, then you can't associate articles to the category. However, it doesn’t affect the existing articles of that category.

</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Configuring Operational Technology Knowledge Management](../concept/configuring-operational-technology-knowledge-management.md)

