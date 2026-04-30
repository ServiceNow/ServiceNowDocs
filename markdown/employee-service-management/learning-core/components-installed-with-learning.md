---
title: Components installed with Learning
description: Several types of components are installed with the activation of Learning, including tables, user roles, and scheduled jobs.
locale: en-US
release: zurich
product: Learning Core
classification: learning-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Learning, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Components installed with Learning

Several types of components are installed with the activation of Learning, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_ddp_3pg_wtb"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_lc.learning\_admin

</td><td>

Sets up Learning application configurations. Performs all the actions in the application. Possesses CRUD access for all tables.

</td><td>

sn\_lc.learning\_admin

</td></tr><tr><td>

sn\_lc.catalog\_group\_manager

</td><td>

Manages catalogs and catalog groups on Learning application.

</td><td>

sn\_lc.catalog\_group\_manager

</td></tr><tr><td>

sn\_lc.learning\_manager

</td><td>

Sets up Learning application configurations. Performs all the actions in the application. Possesses CRUD access for all tables.

</td><td>

sn\_lc.learning\_manager

</td></tr><tr><td>

sn\_lc.catalog\_manager

</td><td>

Manages catalogs on Learning application.

</td><td>

sn\_lc.catalog\_manager

</td></tr><tr><td>

sn\_lc.task\_creator

</td><td>

Responsible for creating learning tasks on Learning application.

</td><td>

sn\_lc.task\_creator

</td></tr><tr><td>

sn\_lep.achievement\_manager

</td><td>

Creates and manages achievements on Learning application.

</td><td>

sn\_lep.achievement\_manager

</td></tr></tbody>
</table>## Tables installed

|Table|Description|
|-----|-----------|
|Achievement \[sn\_lep\_achievement\]|Stores details of all achievements configured on Learning.|
|User achievement \[sn\_lep\_user\_achievement\]|Stores information of all user achievements on Learning.|
|Achievement rule \[sn\_lep\_achievement\_rule\]|Defines the rules to define achievements on Learning.|
|Achievement rule item \[sn\_lep\_achievement\_rule\_item\]|Stores information of all the achievement rules on Learning.|
|Achievement skill \[sn\_lep\_m2m\_achievement\_skill\]|Maps the achievements to the associated skill.|

**Parent Topic:**[Learning reference](learning-experience-reference.md)

