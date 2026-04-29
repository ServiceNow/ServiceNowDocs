---
title: Components installed with Learning Core
description: Several types of components are installed with activation of the Learning Core \[sn\_lc\] plugin, including user roles, and tables.
locale: en-US
release: australia
product: Learning Core
classification: learning-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Learning Core Reference, Learning Core, HR Service Delivery, Employee Service Management]
---

# Components installed with Learning Core

Several types of components are installed with activation of the Learning Core \[sn\_lc\] plugin, including user roles, and tables.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Learning admin \[sn\_lc.learning\_admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) catalog, learning content, learning course catalogs, roles, and configure learning source.

</td><td>

-   sn\_lc.catalog\_manager
-   sn\_hr.integr\_fw.admin

</td></tr><tr><td>

Learning course catalog admin \[sn\_lc.learning\_course\_catalog\_admin\]

</td><td>

Posesses admin rights to manage learning course catalogs.

</td><td>

\[sn\_lc.learning\_course\_catalog\_admin\]

</td></tr><tr><td>

Learning content writer \[sn\_lc.content\_writer\]

</td><td>

Grants read or write access for learning courses.

</td><td>

sn\_lc.content\_creator

</td></tr><tr><td>

Learning task creator \[sn\_lc.task\_creator\]

</td><td>

Grants read or write access for learning tasks.

</td><td>

\[sn\_lc.task\_creator\]

</td></tr><tr><td>

Learning catalog manager \[sn\_lc.catalog\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning libraries.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr><tr><td>

Learning catalog group manager \[sn\_lc.catalog\_group\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning libraries based on groups.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr></tbody>
</table><table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Learning External Content\[sn\_lc\_external\_content\]

</td><td>

Stores details of external course items that are pulled from third-party systems.

</td></tr><tr><td>

Learning User Course Activity\[sn\_lc\_user\_course\_activity\]

</td><td>

Stores details of learning course activities such as user to whom the course is assigned, status, due date, and name of the learning course.

</td></tr><tr><td>

Collection \[sn\_lc\_collection\]

</td><td>

Stores details of the collections of internal and external learning content.

</td></tr><tr><td>

Learning Course Catalog \[sn\_lc\_course\_catalog\]

</td><td>

Stores details of the course catalogs that maintain courses under one category and drive access control

</td></tr><tr><td>

Learning Content\[sn\_lc\_content\]

</td><td>

Stores details of internal learning content such as knowledge articles and videos that are created in the ServiceNow application.

</td></tr><tr><td>

Learning Course Item\[sn\_lc\_course\_item\]

</td><td>

Stores details of learning course items, such as the source to which the learning course belongs.

</td></tr><tr><td>

Learning Task\[sn\_lc\_learning\_task\]

</td><td>

Stores details of learning tasks, such as a user to whom the learning task assigned, and due date by when the learning task must be completed.

</td></tr><tr><td>

Learning System Configuration\[sn\_lc\_learning\_system\_configuration\]

</td><td>

Stores configuration parameters of sources, third-party learning management systems.

</td></tr></tbody>
</table>**Parent Topic:**[Learning Core Reference](learning-core-reference.md)

**Related topics**  


[Course catalog form](course-catalog-table.md)

[Learning library form](learning-library-form.md)

[Learning task form](learning-task-form.md)

[Life-cycle stages of a content collection in Learning Core](lifecycle-stages-collection.md)

[Learning internal content form](learning-internal-content-form.md)

[Learning External Contents form](learning-external-contents-form.md)

[Collection form](collection-form-lc.md)

