---
title: Map a related item in Agent Workspace
description: Manually map catalog items related to a knowledge article in Agent Workspace to enable employees to request the related catalog item.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Map a related item in Agent Workspace

Manually map catalog items related to a knowledge article in Agent Workspace to enable employees to request the related catalog item.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article for which you want to add related articles.

Role required: agent\_workspace\_user

## About this task

This task provides steps to map related catalog items when editing an article in Agent Workspace. You can also map related catalog items when editing an article from the Knowledge Management application in the ServiceNow AI Platform interface. For more information, see [Map catalog items related to an article](map-related-items.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge** &gt; **Published** for a published article or **Lists** &gt; **Knowledge** &gt; **Unpublished** for an unpublished article.

3.  Click the link to the knowledge article for which you want to map a related item.

4.  On the Knowledge form, click the Related Catalog Items related list.

5.  Click **New**.

6.  On the Related Catalog Items form, fill in the fields.

<table id="table_qvl_phn_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to enable the mapping to the related catalog item.

</td></tr><tr><td>

Catalog item

</td><td>

Catalog item related to the knowledge article.You can click the search for record icon \(![Search for Record icon](../image/lookup-icon.png)\) to access a list of available catalog items.

</td></tr><tr><td>

Knowledge article

</td><td>

Number of the knowledge article for which you are adding the related catalog item.

</td></tr><tr><td>

Order

</td><td>

Order in which you want the catalog item to appear in the Related Items section on the Knowledge Management article view page. A lower value means that a catalog item has the greater priority to appear in the Related Items section. The default value is 100.

</td></tr></tbody>
</table>7.  Click **Save**.


## Result

The mapped catalog items are listed in the Related Items section on the Knowledge Management article view page in Knowledge Management Service Portal.

**Note:** Because system administrators can configure the number of catalog items shown in the Related Items section, not all mapped related catalog items might appear in the Related Items section. For more information, see [Configure related catalog item widget instance options](configure-related-items-widget.md).

**Related topics**  


[Edit a knowledge article in Agent Workspace](edit-article-workspace.md)

[Service Catalog items](../../service-catalog-management/concept/c_IntroductionToCatalogItems.md)

