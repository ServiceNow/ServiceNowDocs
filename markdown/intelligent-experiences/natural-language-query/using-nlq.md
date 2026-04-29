---
title: Using Natural Language Query
description: With Natural Language Query \(NLQ\), you can query data in your tables by entering requests in natural, everyday language.
locale: en-US
release: australia
product: Natural Language Query
classification: natural-language-query
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Natural Language Query, Enable AI experiences]
---

# Using Natural Language Query

With Natural Language Query \(NLQ\), you can query data in your tables by entering requests in natural, everyday language.

## NLQ overview

NLQ turns your plain-language requests into structured queries of your data. You don't need to know how to use the condition builder, because NLQ constructs and displays the conditions for you.

If you have a role such as itil that can view and interact with tables, you can use NLQ by selecting the natural language filter icon.

NLQ works on any list on the platform. It returns results only from the table or list you query on.

## Find and use the natural language filter

Selecting the natural language filter icon brings up the NLQ interface.

![NLQ interface in list view.](../images/using-nlqT1.png)

Enter your request in the What do you want to see field, then select **Ask**. NLQ parses your request, then displays the query in the condition builder. The results of the query are displayed in the list.

With the default configuration of NLQ, you can continue to refine your query by entering another request into the What do you want to see field.

![Using NLQ to append a query to a previous query](../images/using-nlq-washingtondc.gif "Using NLQ to build on a previous query")

This example image and procedure illustrates how to build a query using NLQ:

1.  On the Incident table in the natural language filter, enter `show me active hardware tickets` and select the **Ask** button.
2.  The condition builder displays **All** &gt; **Active = true** &gt; **Category = Hardware** as the query. The filtered results are displayed in the list.
3.  To narrow down the list of results further, enter `without assignment group`. Notice that as you type, NLQ displays possible matches for columns and fields. Select assignment group from the list of suggestions, and then **Ask**.
4.  In the condition builder, NLQ adds **&gt;Assignment group is empty** to the query. The list refreshes to display only the matching rows.
5.  To reset and start a new query, delete everything in the condition builder so that only **All** remains.

## Useful information

Keep the following information in mind when using NLQ.

-   Your requests can contain periods and apostrophes, but not wildcard characters such as asterisks or regex.
-   To group by a field or column, that column must be visible in the list view. Use the personalize list icon \(![Personalize list icon.](../../../common/image/List_PersonalizeListIcon.png)\) to hide or display columns.
-   For information about querying CMDB tables, see [Querying the CMDB](https://www.servicenow.com/docs/access?context=querying-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Tips for improving your queries

When you select the **Tips for improving your queries** button, a modal window appears in the user interface. This window offers the following information about terms you can use in your NLQ questions and requests:

-   Sorting or grouping: grouped by; sorted by; A-Z; z-a
-   Dates: today; yesterday; last; this; next day\(s\); week\(s\); quarter\(s\); year\(s\)
-   Filtering: starts with; ends with; more than; less than; empty; not empty; and; or
-   Other information: my; my team; created by; unassigned

|Query|Example|
|-----|-------|
|Sorting or grouping|incidents grouped by category|
|Dates|created last month|
|Filtering|short description starts with computer|
|Other information|unassigned tickets|
|Single number|INC0777|

