---
title: Scope entities to discover processing activities with personal information
description: Determine which entities have and process personal information using the ServiceNow Configuration Management Database \(CMDB\) application.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Entity scoping to plan a privacy program, Use, Privacy Management, Governance, Risk, and Compliance]
---

# Scope entities to discover processing activities with personal information

Determine which entities have and process personal information using the ServiceNow® Configuration Management Database \(CMDB\) application.

## Before you begin

Ensure that you created the CMDB queries. For more information on the CMDB queries, see [Querying the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/querying-cmdb.md).

Role required: sn\_privacy.manager

## About this task

In the Configuration Management Database \(CMDB\), you can search the database for entities that process personal data using one of the following methods:

-   Using the predefined queries and selecting only those applications and processes that have associated information objects. For more information about information objects and their role in Privacy Management, see [Information objects in Privacy Management](../concept/information-object-in-privacy.md). For information on how to scope entities with personal information, see [Scope entities to discover processing activities with personal information](scope-entities-with-pi.md)
-   Building your own query. For more information on building the CMDB queries, see [Querying the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/querying-cmdb.md)

To filter entities that contain personal data, you must filter the entities using the appropriate queries. ServiceNow® provides two default queries for you to use to filter entities with personal data. The default queries are provided for the following tables:

-   Business process
-   Business application

You can also create your own queries. This procedure demonstrates using the default queries.

## Procedure

1.  Navigate to **All** &gt; **Privacy Workspace** &gt; **Scoping** &gt; **Entity types**.

2.  Open the entity you want to filter for personal information.

3.  Click the Entity Filters related list.

4.  Click **New**.

    The Entity Filter form is displayed.

5.  In the Filter conditions section, in the **Entity filter type** field, select **Select from predefined queries**.

6.  In the Query field, select **Business applications by IO**.

    The **Table** field is automatically set.

7.  To add more information objects that contain personal information such as email address, click **Information objects** and type `Email`.

8.  Click **Submit**.


## Example

![Predefined queries with associated information objects.](../image/entity-filters-io.png "Usage of predefined queries")

**Parent Topic:**[Entity scoping to plan a privacy program](../concept/entity-scoping-in-privacy-mgmt.md)

