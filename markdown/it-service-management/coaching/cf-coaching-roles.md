---
title: Coaching roles
description: Assign Coaching roles to specify what different users can see and do.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Coaching, IT Service Management]
---

# Coaching roles

Assign Coaching roles to specify what different users can see and do.

<table id="table_nqm_rvp_2fb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Roles inherited

</th></tr></thead><tbody><tr><td>

sn\_coaching.trainee\[Coaching trainee\]

</td><td>

Able to view coaching assessments to which they belong.

 Able to add work notes in a coaching assessment by clicking **Review Assessments**.

</td><td>

-   skill\_user
-   survey\_reader
-   pa\_viewer

</td></tr><tr><td>

sn\_coaching.coach\[Coaching coach\]

</td><td>

Able to read and write coaching assessments assigned to the coach group to which they belong.

 Able to assign a training and virtual coaches to a coaching opportunity.

**Note:** The Coaching coach is not able to create a new coaching opportunity.

</td><td>

-   sn\_coaching.trainee
-   pa\_viewer
-   sn\_lc.catalog\_manager

</td></tr><tr><td>

sn\_coaching.admin\[Coaching admin\]

</td><td>

Able to perform all functions.

</td><td>

-   sn\_coaching.coach
-   survey\_admin
-   sn\_cim\_improvement\_requester
-   sn\_lc.learning\_admin

</td></tr><tr><td>

Learning catalog group manager \[sn\_lc.catalog\_group\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning libraries based on groups.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr></tbody>
</table>**Parent Topic:**[Coaching reference](cf-coaching-reference.md)

