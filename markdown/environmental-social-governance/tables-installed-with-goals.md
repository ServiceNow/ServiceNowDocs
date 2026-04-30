---
title: Roles installed with the Goal Framework
description: Several roles are installed with activation of the Goal Framework plugin.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Operational Sustainability Management \(formerly ESG\) reference, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Roles installed with the Goal Framework

Several roles are installed with activation of the Goal Framework plugin.

## Roles installed

<table id="table_ktr_yyj_jrb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_gf.goal\_user\_read

</td><td>

Can view the goals. This role can be given to users such as project user and demand user.

</td><td>

None

</td></tr><tr><td>

sn\_gf.goal\_user

</td><td>

Can create, view, edit, and delete goals, sub-goals, and associated targets.**Note:**

-   A goal or sub-goal can be deleted only by the owner and contributors when the sn\_gf.allow\_goal\_deletion system property is set to **Yes**.
-   An associated target can be deleted only by the owner and contributors when the sn\_gf.allow\_goal\_deletion system property is set to **Yes**.
-   A goal or target can be edited only by the respective owner and contributors of the goal and target.

</td><td>

sn\_gf.goal\_user\_read

</td></tr><tr><td>

sn\_gf.goal\_admin

</td><td>

Can update the goal preferences.

</td><td>

-   sn\_gf.goal\_user\_read
-   sn\_gf.goal\_user

</td></tr><tr><td>

sn\_gf.strategy\_planner\_read

</td><td>

Can view all strategic plans and strategic values.

</td><td>

None

</td></tr><tr><td>

sn\_gf.strategy\_planner

</td><td>

Can create, view, edit, and delete strategic plans and strategic values.**Note:**

-   A strategic plan can be edited only by the owner and sponsor of the strategic plan.
-   A strategic value can be edited only by the sponsor of the strategic plan.

</td><td>

sn\_gf.strategy\_planner\_read

</td></tr><tr><td>

sn\_gf.epmo\_strategy\_planner

</td><td>

Can create, view, edit, and delete any goal.

</td><td>

-   sn\_gf.goal\_user\_read
-   sn\_gf.goal\_user
-   sn\_gf.goal\_admin
-   sn\_gf.strategy\_planner

</td></tr></tbody>
</table>**Parent Topic:**[Operational Sustainability Management \(formerly ESG\) reference](../concept/reference-data-esg.md)

