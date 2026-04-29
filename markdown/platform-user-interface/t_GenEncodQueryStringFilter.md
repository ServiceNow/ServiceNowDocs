---
title: Generate an encoded query string through a filter
description: You can generate an encoded query string through a filter on any list and paste the string into a URL query or a reference qualifier.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Encoded query strings, Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Generate an encoded query string through a filter

You can generate an encoded query string through a filter on any list and paste the string into a URL query or a reference qualifier.

## Before you begin

Role required: none

## Procedure

1.  Open a list of records.

2.  [Construct the filter](t_CreatingFilters.md).

3.  Click **Run**.

4.  Right-click the end of the filter breadcrumb and select **Copy query** from the context menu.

    ![Copy the query](../image/FilterToQuery2.png "Copy the query from the breadcrumb")

    If you are in split mode in List v3, right-click the blue filter text in the left pane.

5.  Copy the query to your system clipboard.

6.  Use the query string to [Navigate to a record or module using a URL](../../navigation/task/navigate-using-url.md) or an [Reference qualifiers](https://www.servicenow.com/docs/access?context=c_ReferenceQualifiers&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    When you use the CONTAINS operator on a list filter, the system translates the filter to a LIKE query. For example, if you filter for active records with numbers that contain 123, the URL is `https://InstanceName.service-now.com/incident_list.do?sysparm_query=active%3Dtrue%5EGOTOnumberLIKE123`.


**Parent Topic:**[Encoded query strings](../concept/c_EncodedQueryStrings.md)

**Related topics**  


[Reference qualifiers](https://www.servicenow.com/docs/access?context=c_ReferenceQualifiers&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Navigate to a record or module using a URL](../../navigation/task/navigate-using-url.md)

