---
title: Searching in Dispatcher Workspace examples
description: Use keyword searches to quickly find resource and agents. Understanding this functionality can greatly reduce the time it takes to find what you’re looking for.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/search-keyword-example.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Searching in Dispatcher Workspace examples

Use keyword searches to quickly find resource and agents. Understanding this functionality can greatly reduce the time it takes to find what you’re looking for.

Depending on your configuration, you might need to set up additional tables for indexing before using keyword searching in Dispatcher Workspace. For example, Territory Planning requires specific table configurations Dispatcher Workspace. For more information, see [Configure keyword searching in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/keywords-dispatcher.md).

1.  Search for an agent in a specific location.

    You can use the Boolean operator AND to find specific agents in a specific location. In the image below, the dispatcher is searching for agents named Lori located in Cupertino. The keyword they enter is `Lori AND Cupertino`.

    \[Omitted image "lori-and-cupertino.png"\] Alt text: lori and cupertino search

2.  Searching for more than one agent.

    You can use the Boolean operator OR to find multiple agents at once. In the image below, the dispatcher is searching for agents named Lori or Brian, so they enter the keyword `Lori OR Brian`.

    You can also use the OR operator to find multiple territories. For example, `TeritoryA OR TerritoryZ`, returns the two territories, TerritoryA and TerritoryZ, in the search results.

    \[Omitted image "lori-or-brian.png"\] Alt text: lori or brian search

3.  Searching for agents, while excluding others.

    Use the Boolean operator NOT to find agents who match one term but not another. In the image below, the dispatcher is looking for agents named Lori who do not have the last name Ferguson. The dispatcher enters the keyword LORI NOT FERGUSON.You can use the operator NOT to find agents who match one term but not another. In the image below, the dispatcher is looking for agents named Lori who don’t have the last name Ferguson. The dispatcher uses the keyword `Lori NOT Ferguson`.

    \[Omitted image "lori-not-ferguson.png"\] Alt text: lori not ferguson search

4.  Searching for agents with just a few characters.

    You can use the wildcard operator \* to find all results that match partial character patterns. In the image below the dispatcher is looking for agents whose names begin with `L` and include an `i` later in the name. The dispatcher uses the keyword `L*i`.

    \[Omitted image "l-star-i.png"\] Alt text: l\*i search

5.  Searching for more than one agent without using the full name.

    You can combine the wildcard operator \* with the Boolean operator OR to find multiple agents without entering their full names. In the image below, the dispatcher is looking for two agents: one whose name starts with `Br` and ends with `n`, and another whose name starts with `sha` and ends with `n`. The dispatcher enters the keyword `br*n OR sha*n`.

    \[Omitted image "br-or-sha.png"\] Alt text: br or sha search

6.  Searching for a work order task by number only.

    You can search for work order tasks by entering the numeric portion of the task number without the WOT prefix. For example, entering 12345 returns WOT00012345. You must enter more than two digits to return work order tasks; for example, entering 45 does not return WOT12345.

    \[Omitted image "task-search-number.png"\] Alt text: task search number


