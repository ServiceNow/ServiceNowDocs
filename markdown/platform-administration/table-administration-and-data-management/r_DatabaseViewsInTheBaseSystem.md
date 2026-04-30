---
title: Database views in the base system
description: Certain views are included in the base system with the Database Views and Database Views for Service Management plugins.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Work with database views, Table admin, Tables and data, Configure core features, Administer]
---

# Database views in the base system

Certain views are included in the base system with the Database Views and Database Views for Service Management plugins.

|Name|Description|Label|
|----|-----------|-----|
|change\_request\_metric|Join change to metric definition to metric instance, creating a view that can be reported on for things like: Changes that were closed by category.|Change Metric|
|change\_request\_sla|Join change\_request to sla\(task\_sla\), creating a view that can be reported on for things like change request resolved by sla per change category.|Change Request SLA|
|change\_task\_metric|Join change task to metric definition to metric instance, creating a view that can be reported on for things like: Change tasks that were closed by change state|Change Task Metric|
|change\_task\_sla|Join change\_task to sla\(task\_sla\), creating a view that can be reported on for things like change tasks resolved by sla.|Change Task SLA|
|change\_task\_time\_worked|Join change task to task time worked to pull time worked entries associated with incidents.|Change Task Time Worked|
|incident\_metric|Join incident to metric definition to metric instance creating a view that can be reported on for things like: Incidents that were resolved on the first call by category|Incident Metric|
|incident\_sla|Join incident to sla\(task\_sla\) to report on things like incidents resolved by sla per incident category.|Incident SLA|
|incident\_time\_worked|Join incident to task time worked to pull time worked entries associated with incidents.|Incident Time Worked|
|pm\_project\_metric|Join pm\_project to metric definition to metric instance creating a view that can be reported on for things like: Projects that were closed by name or date|Project Metric|
|pm\_project\_sla|Join pm\_project to sla\(task\_sla\) to report on things like project names by sla.|Project SLA|
|pm\_project\_task\_metric|Join pm\_project\_task to metric definition to metric instance creating a view that can be reported on for things like: Project tasks that were closed by name or date|Project Task Metric|
|pm\_project\_task\_sla|Join pm\_project to sla\(task\_sla\) to report on things like release tasks by sla.|Project Task SLA|
|pm\_project\_task\_time\_worked|Join pm\_project\_task to task time worked to pull time worked entries associated with project tasks.|Project Task Time Worked|
|problem\_metric|Join problem to metric definition to metric instance creating a view that can be reported on for things like: Problems that were resolved on the first call by category|Problem Metric|
|problem\_sla|Join problem to sla\(task\_sla\) to report on things like problems resolved by sla per problem state.|Problem SLA|
|release\_feature\_metric|Join release\_feature to metric definition to metric instance creating a view that can be reported on for things like: Release Features that were closed by product|Release Feature Metric|
|release\_project\_metric|Join release\_project to metric definition to metric instance creating a view that can be reported on for things like: Releases that were closed by category|Release Metric|
|release\_task\_metric|Join release\_task to metric definition to metric instance creating a view that can be reported on for things like: Release Features that were closed by feature|Release Task Metric|
|release\_task\_sla|Join release\_task to sla\(task\_sla\) to report on things like release tasks by sla.|Release Task SLA|
|sc\_request\_metric|Join sc\_request to metric definition to metric instance creating a view that can be reported on for things like: Requests that were closed by category|Catalog Request Metric|
|sc\_request\_sla|Join sc\_request to sla\(task\_sla\) to report on things like requests by sla.|Catalog Request SLA|
|sc\_req\_item\_metric|Join sc\_request\_item to metric definition to metric instance creating a view that can be reported on for things like: Request Items that were closed by item|Catalog Request Item Metric|
|sc\_req\_item\_sla|Join sc\_req\_item to sla\(task\_sla\) to report on things like request items by sla.|Catalog Request Item SLA|
|sc\_task\_metric|Join sc\_task to metric definition to metric instance creating a view that can be reported on for things like: Catalog tasks that were closed by item|Catalog Task Metric|
|sc\_task\_sla|Join sc\_task to sla\(task\_sla\) to report on things like tasks by sla.|Catalog Task SLA|

**Parent Topic:**[Working with database views for reporting](../concept/c_DatabaseViews.md)

**Related topics**  


[Joining tables using database views](../task/c_CreatingDatabaseViews.md)

[Displaying function results in a database view](../task/displaying-function-results-in-a-database-view.md)

[Using disjunctions in complex queries](../concept/c_UseDisjunctionsInComplexQueries.md)

