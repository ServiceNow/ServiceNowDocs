---
title: Create a custom knowledge homepage
description: As a system administrator, you can create a module allowing users to open a knowledge homepage for a specific knowledge base or category.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a custom knowledge homepage

As a system administrator, you can create a module allowing users to open a knowledge homepage for a specific knowledge base or category.

## Before you begin

Role required: admin

## About this task

**Note:** This topic creates a legacy v3 knowledge homepage. You can create a portal homepage and configure it to get a new look and feel. For information, see [Configure the Knowledge Management Service Portal](../concept/knowledge-management-service-portal.md).

## Procedure

1.  In the application navigator, point to the application name and click the edit application icon \(![Edit Application icon](../image/edit-app.png)\).

2.  In the **Modules** related list click **New**.

3.  Enter a **Title** for the module.

4.  In the **Link type** field, select **URL \(from Arguments\)**.

5.  In the **Arguments** field, append one or more of the following values to `$knowledge.do#/search?`.

<table id="choicetable_c4x_2q1_5r"><tbody><tr><td id="d397503e121">

**sysparm\_kb=&lt;knowledge base sys\_id&gt;**

</td><td>

Enter the sys\_id of a knowledge base to show knowledge articles from that knowledge base by default.

 If the specified knowledge base does not exist, the default knowledge homepage appears when accessing the custom homepage module.

</td></tr><tr><td id="d397503e136">

**sysparm\_category=&lt;knowledge category sys\_id&gt;**

</td><td>

Enter the sys\_id of a knowledge category to show knowledge articles from that category by default.

 If the specified category does not exist, the default category for the selected knowledge base appears when accessing the custom homepage module.

**Note:** The category passed in this parameter must belong to the knowledge base passed in the **sysparm\_kb** parameter.

</td></tr><tr><td id="d397503e156">

**sysparm\_order=&lt;view\_count, last\_modified, or relevancy&gt;**

</td><td>

Enter the default sort order for articles to appear in.

</td></tr></tbody>
</table>
## Example

**Related topics**  


[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)

[I18N - Knowledge internationalization](../concept/c_I18NKMInternational.md)

