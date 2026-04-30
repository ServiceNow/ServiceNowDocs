---
title: Plan sprints
description: Streamline your sprint planning and completion activities using the Sprint Planning tab.
locale: en-US
release: zurich
product: PPM Collaboration
classification: ppm-collaboration
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Agile Development 2.0 integration with Project Portfolio Management, Explore, Project Portfolio Management, Strategic Portfolio Management]
---

# Plan sprints

Streamline your sprint planning and completion activities using the **Sprint Planning** tab.

## Before you begin

Role required: scrum\_admin, scrum\_master, or scrum\_sprint\_planner

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Groups**.

2.  Open the desired group.

3.  Click the **Plan Sprints** related link.

    The Agile Board, **Sprint Planning** tab appears.

4.  Use either of options to view all the active stories assigned to the team, but not assigned to any sprint in the Backlog section.

<table id="choicetable_pgt_smy_p1b"><thead><tr><th align="left" id="d115411e94">

Action

</th><th align="left" id="d115411e97">

Description

</th></tr></thead><tbody><tr><td id="d115411e103">

**Using the drag feature**

</td><td>

This option can be used to move stories within the backlog, move stories from the backlog to any sprint, or move stories from one sprint to another. Point to a story in the backlog and drag it to the required location.

</td></tr><tr><td id="d115411e115">

**Using the keyboard**

</td><td>

This option can be used to move stories only within a backlog or a sprint.

</td></tr></tbody>
</table>    **Note:**

    -   If the backlog contains more than 50 stories, then pagination control appears at the bottom of the list enabling you to navigate to the previous, next, first, or last pages in the list.
    -   Rearranging stories in the backlog changes the ranking of stories. Ranks are stored in the global\_rank column in the Story \[rm\_story\] table. When you move a story within a backlog, its rank changes relative to the stories within the same backlog. Thus, if the story exists in some other backlog, its ranking might change but position in the backlog would remain the same.
5.  To start a sprint, click **Start** that appears at right-corner of the first or top sprint.

    The**Sprint Tracking** tab appears.

6.  To complete a sprint, click **Complete Sprint** that appears at right-corner of the first or top sprint.

    1.  Move incomplete stories, if any, to the backlog or a future sprint.

    2.  Click **Complete**.

        The sprint disappears from the **Sprint Planning** tab and appears in the Sprint list as complete.


**Parent Topic:**[Agile Development 2.0 integration with Project Portfolio Management](../../sdlc-scrum/concept/c_SDLCIntegrationWithProjectPortfolioSuite.md)

