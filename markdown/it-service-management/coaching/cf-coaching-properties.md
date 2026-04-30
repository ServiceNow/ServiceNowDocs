---
title: Coaching properties
description: Set the duration to read knowledge articles and whether to exclude weekends for trainees to complete training using Coaching properties.
locale: en-US
release: zurich
product: Coaching
classification: coaching
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Coaching, IT Service Management]
---

# Coaching properties

Set the duration to read knowledge articles and whether to exclude weekends for trainees to complete training using Coaching properties.

These properties are available for Coaching.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_j5m_whs_tcc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.sn\_coaching\_assessment\_activity.fields

</td><td>

Edit coaching assessment activities.-   **Type:** string
-   **Default value:** assigned\_to,cmdb\_ci,state,impact,priority,opened\_by,work\_notes,comments,\*Attachments\*,assessment\_of

</td></tr><tr><td>

sn\_coaching.recommended\_learning\_deprecated

</td><td>

Coaching Recommended Trainings is being deprecated and replaced with the Learning Tasks and course items from Coaching with Learning.-   **Type:** string
-   **Default value:** true

</td></tr><tr><td>

sn\_coach.lrn.exclude\_weekends\_on\_learning\_task\_due\_date

</td><td>

Enable property to exclude weekends while setting the due date for learning tasks.-   **Type:** true\|false
-   **Default value:** true

</td></tr><tr><td>

sn\_coach\_lrn.learning\_list\_menu\_props

</td><td>

Data array properties for the now-list-menu component on the Learning Tasks tab, coaching module.-   **Type:** string
-   **Default value:** script for data array

</td></tr><tr><td>

sn\_coaching.kb\_article\_duration

</td><td>

Number of days to read the knowledge article. **Note:** The admin \(sn\_wfo.admin\) sets the number of days for the trainee to complete reading the article. The number of days is converted to the due date for the trainee to complete the training. It is calculated from the current date taking the trainee's time zone into consideration.

-   **Type:**Integer
-   **Default value:**5

</td></tr><tr><td>

sn\_coaching.exclude\_weekends\_on\_training\_due\_date

</td><td>

Excludes weekends when the due date is set for trainees to complete training.-   **Type:**true \| false
-   **Default value:**true

</td></tr></tbody>
</table>**Parent Topic:**[Coaching reference](cf-coaching-reference.md)

