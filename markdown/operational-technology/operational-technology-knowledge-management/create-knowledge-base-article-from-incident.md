---
title: Create a knowledge article from an OT incident record
description: Create a knowledge article to record and save information that is related to an Operational Technology \(OT\) incident and its resolution.
locale: en-US
release: australia
product: Operational Technology Knowledge Management
classification: operational-technology-knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Knowledge Management, Operational Technology]
---

# Create a knowledge article from an OT incident record

Create a knowledge article to record and save information that is related to an Operational Technology \(OT\) incident and its resolution.

## Before you begin

Role required: sn\_ot\_incident\_write

**Note:** You also need the **Can contribute** access to at least one knowledge base. For more information, see [Create an OT knowledge base](configure-ot-knowledge-base.md).

## About this task

Creating a knowledge article directly from an incident record helps to make sure that the knowledge article is linked to the correct incident for contextual information. The knowledge article can also help your team resolve similar incidents in the future when they include the correct procedures, challenges, and solutions.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  In the list view under the OT Incident module, open one of the available lists.

3.  Select the OT incident record that you want to create a knowledge article for.

4.  Select the **More actions** icon \(![More actions icon](../image/more-actions.png)\) to expand the menu.

5.  Select **Create Knowledge**.

    **Note:** You must set the incident record's state to **Resolved** to see the **Create Knowledge** button.

6.  On the form, fill in the fields.

<table id="table_df1_vrm_bzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge base

</td><td>

Knowledge base that the knowledge article should be included in.**Note:** If you configured the OT knowledge base's visibility correctly, OT users can find the knowledge base in this reference list.

</td></tr><tr><td>

Category

</td><td>

Classification of the knowledge article.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the incident resolution that is used as the knowledge article title.

</td></tr><tr><td>

Article body

</td><td>

Content of the knowledge article that describes any procedures, challenges, and solutions for the incident.

</td></tr><tr><td>

Valid to

</td><td>

Date that the knowledge article is valid until.

</td></tr></tbody>
</table>7.  Select **Save**.

    The knowledge article is saved as a draft and attached to the parent OT incident.

8.  Select **Publish**.


## Result

The knowledge article is now published in your OT knowledge base. To view the knowledge article, open the Attached Knowledge related list in the incident record.

**Note:** If you set the **Publish workflow** field in your OT knowledge base to **Knowledge - Approval Publish**, the article must be approved before being published.

**Parent Topic:**[Using Operational Technology Knowledge Management](../concept/using-operational-technology-knowledge-management.md)

