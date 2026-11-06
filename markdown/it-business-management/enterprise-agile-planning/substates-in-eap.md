---
title: Substates in EAP
description: Divide a story state into substates in Enterprise Agile Planning so that a team can track work in more detail.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/enterprise-agile-planning/substates-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-10-14"
reading_time_minutes: 3
keywords: [substates, story states, Team Settings, Planning board]
breadcrumb: [Explore, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Substates in EAP

Divide a story state into substates in Enterprise Agile Planning so that a team can track work in more detail.

Story states are the same for every team, but teams don't all work in the same steps. When a team does several kinds of work within one state, the Planning board shows a single lane for all of it. The team can't see where in the state its work is waiting.

A substate helps divide a story state into smaller steps that match how a team works. For example, a team can divide the **Work in progress** state into **Code review** and other steps. Each substate belongs to one team and one state, so each team defines the substates that fit its own process. Other teams and their states aren't affected.

A scrum master creates and manages substates from the **Substates** tab of the Team Settings page. For more information, see [Create substates for a team in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/create-substates-for-a-team-in-eap.md).

## Benefits of substates

Substates give a team a closer view of its work while the standard states stay the same:

-   A story keeps its state. Substates add detail within the state, so planning that relies on states continues to work.
-   Each team sets its own substates. A change by one team doesn't affect the substates of another team.
-   The Planning board of the team shows one lane for each substate, so the team can see where work is waiting within a state.
-   A team can set a WIP limit on a single substate lane, such as **Code review**, to keep work from piling up at one step. For more information, see [Set WIP limits for Kanban lanes in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/set-wip-limits-for-kanban-lanes-in-eap.md).

## What defines a substate

Each substate has a state that it belongs to, a name that users see, and an order. Substates with lower order numbers appear first within the state. A substate can also be the default for its state.

For the fields that you complete when you create a substate, see [Create substates for a team in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/create-substates-for-a-team-in-eap.md).

## Default substates

A team can have one default substate for each state. The first substate that you create for a state becomes the default automatically, even if you don't select **Use as default**. A state that has substates therefore always has a default substate. If you mark a different substate as the default, the new default replaces the previous one, and a message tells you about the change.

When the first default substate is set for a state, the stories in that state that have no substate are moved to it. This update runs in the background, and a message tells you that it started.

## Substates on stories

Story forms and lists have a **Substate** field. The field lists the substates of the story's team for the story's current state. The field doesn't appear when the team has no substates for the state. It also doesn't appear for a story that belongs to a team above the Agile Team level in the Agile structure.

The substate of a story follows its state:

-   When you change the state of a story, the substate changes to the default substate of the new state. If the new state has no substates, the field is cleared.
-   If you change the state and choose a substate in the same update, your chosen substate is kept.
-   If you change only the substate, the state changes to the state that the substate belongs to.

## Substates on the Planning board

On the Planning board of a team, a state that has substates shows one lane for each substate in place of the lane for the state. Each lane header shows the substate name, the number of stories in the lane, and the state that the substate belongs to. After you create the first substate for a state, the lane might be empty until the background update finishes. Refresh the board to see the stories that moved to the default substate.

\[Omitted image "eap-planning-board-substates-wip-limits.png"\] Alt text: Planning board with Design Ready and Code review substate lanes, each showing the state it belongs to, next to the other state lanes.

