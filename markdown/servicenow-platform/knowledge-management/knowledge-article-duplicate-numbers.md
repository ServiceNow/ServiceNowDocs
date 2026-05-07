---
title: Duplicate knowledge article numbers
description: Importing knowledge articles into an instance can create articles with duplicate numbers.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Duplicate knowledge article numbers

Importing knowledge articles into an instance can create articles with duplicate numbers.

The Knowledge **Number** field is auto-generated and is incremented every time you create a new article in an instance. The initial value for the **Number** field is 10,000. To customize this number:

1.  Navigate to **System Definition** &gt; **Number Maintenance**.
2.  In the **Table** column, search for and select **Knowledge**.
3.  Under **Related Links** select **Number Counter**, then update the Number field.
4.  Select**Update**.

Importing knowledge articles from another instance or as part of the demo data for another application may introduce an article with a number that is already in use. Because the Knowledge **Number** field is not uniquely indexed, the import completes without error.

With duplicate knowledge article numbers present, links to article view pages that use the knowledge number can behave inconsistently. For example, if there are two articles with the same Knowledge number KB0000033, the following link may open either of these two articles randomly: **kb\_view.do?sysparm\_article=KB0000033**. This can happen in Knowledge search results where clicking on a result opens a different article instead of the article displayed in the search results.

## Avoiding duplicate Knowledge article numbers

To avoid inserting Knowledge articles with duplicate numbers into a production environment:

-   Do not import demo data articles in production environment.
-   Verify the numbers of the articles to be inserted to make sure they are not already in use.
-   Create a before insert business rule on the Knowledge table \(kb\_knowledge\) to ensure the new number is not already in use.

You can also update the initial value for the Knowledge **Number** field so that newly created articles do not conflict with existing articles.

1.  Navigate to **System Definition** &gt; **Number Maintenance**.
2.  In the **Table** column, search for and select **Knowledge**.
3.  In the Controls related list, in the **Number** field, update the count to a number greater than the largest value already in the system.
4.  Click **Update**.

**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)

