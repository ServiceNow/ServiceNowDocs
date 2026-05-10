---
title: Components installed with Scrum Programs
description: Understand the roles, tables, business rules, and UI macros that are installed when you activate the Scrum Programs plugin.
locale: en-US
release: australia
product: Agile Development
classification: agile-development
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scrum Programs for Agile Development 2.0, Agile Development, Strategic Portfolio Management]
---

# Components installed with Scrum Programs

Understand the roles, tables, business rules, and UI macros that are installed when you activate the Scrum Programs plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles installed with Scrum Programs

<table id="table_on5_zld_pkb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Program manager \[it\_program\_manager\]

</td><td>

Users with this role have full control on all the scrum programs.

</td><td>

-   program\_manager
-   scrum\_product\_owner
-   scrum\_master

</td></tr></tbody>
</table>**Note:** The it\_program\_manager role is installed with the activation of Scrum Programs only if it is not already installed through the Project Portfolio Management plugin.

## Tables installed with Scrum Programs

|Table|Description|
|-----|-----------|
|epic\_backlog\_definition|Stores the filter criteria that is used to create the epic backlogs.|
|scrum\_program\_m2m\_group|Stores the relationship between a scrum program and its teams.|

## Business rules installed with Scrum Programs

|Name|Table|Description|
|----|-----|-----------|
|Set global rank for epic|rank\_configuration|Contains fix script to populate global rank for existing epics.|

## UI macros installed with Scrum Programs

<table id="table_olq_4pd_pkb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

program\_planning\_constants

</td><td>

Contains customizable TEAM\_LIMIT and STORY\_LIMIT properties.

 These properties limit the number of teams and stories that can be shown on the scrum program planning board.

</td></tr></tbody>
</table>The default value for the TEAM\_LIMIT property is 15 and STORY\_LIMIT property is 1000. You can change these values according to your preferences.

**Note:** Increasing the values might result in longer loading times and degraded performance of the scrum program planning board.

**Parent Topic:**[Scrum Programs for Agile Development 2.0](../concept/scrum-programs-concept.md)

