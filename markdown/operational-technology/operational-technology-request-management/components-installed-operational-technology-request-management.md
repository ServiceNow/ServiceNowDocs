---
title: Components installed with Operational Technology Request Management
description: Several types of components may be installed with the activation of Operational Technology Request Management, including user roles and service catalogs.
locale: en-US
release: yokohama
product: Operational Technology Request Management
classification: operational-technology-request-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Request Management, Operational Technology]
---

# Components installed with Operational Technology Request Management

Several types of components may be installed with the activation of Operational Technology Request Management, including user roles and service catalogs.

## Roles installed

<table id="table_nnd_j2d_r1c"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_request\_read

</td><td>

Read access to the Request \(sc\_request,\) Requested Item \(sc\_req\_item\) or Catalog Task \(sc\_task\).

</td><td>

NA

</td></tr><tr><td>

sn\_request\_write

</td><td>

Write access to the Request \(sc\_request,\) Requested Item \(sc\_req\_item\), or Catalog Task \(sc\_task\).

</td><td>

-   task\_editor
-   dependency\_views
-   agent\_workspace\_user
-   view\_changer
-   cmdb\_read
-   cmdb\_query\_builder\_read
-   sn\_request\_read

</td></tr><tr><td>

sn\_request\_comment\_write

</td><td>

Write access to the comments for the Requested Item \(sc\_req\_item\).**Note:** The sn\_request\_comment\_write role alone does not give access to comments write, you will need write access for the table.

</td><td>

NA

</td></tr></tbody>
</table>## Service catalogs installed

|Name|Description|
|----|-----------|
|OT Service Catalog|Service catalog provided for users to submit OT requests.|

**Parent Topic:**[Operational Technology Request Management reference](../concept/operational-technology-request-management-reference.md)

