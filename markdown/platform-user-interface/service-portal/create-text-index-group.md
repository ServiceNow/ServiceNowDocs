---
title: Add a text index group to a portal
description: Define how users see search results. For example, combine search results from several sources, or set the weight of certain fields.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Add a text index group to a portal

Define how users see search results. For example, combine search results from several sources, or set the weight of certain fields.

## Before you begin

Role required: admin

If you have a custom search source or portal, consider whether you want to use the base system **portal\_index\_group** text index group, or create your own text index group. The base system text index group includes the Catalog items and Knowledge tables. When a user searches for an item in Service Portal, they see combined results from these tables.

**Note:** Index tables before adding them to a text index group. To learn more about text indexing, see [Configure a table for indexing and searching](https://www.servicenow.com/docs/access?context=configure-single-table-for-indexing&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Text index groups are a ServiceNow AI Platform feature. To learn more, see [Configure multiple tables for indexing and searching](https://www.servicenow.com/docs/access?context=index-multiple-tables&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## About this task

**Note:** Text index groups do not support external search sources.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Open the portal that you would like to add a text index group to.

3.  Configure the form to add the **Text Index Group** field.

4.  Add the text index group you want to the **Text Index Group** field.


## Result

Search results display according to the text index group's rules.

**Parent Topic:**[Zing search in Service Portal](../concept/zing-search-service-portal.md)

