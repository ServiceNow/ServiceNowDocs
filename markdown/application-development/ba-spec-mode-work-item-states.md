---
title: Autonomous Engineer plan and work item states
description: Plan and work item states appear during planning and execution. Identify where a plan or work item is in the execution process and what action is required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ba-spec-mode-work-item-states.html
release: brazil
topic_type: reference
last_updated: "2026-09-09"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, Autonomous Engineer, work item states, plan states, plan dashboard, plan execution, background agent, ATF tests, update set, draft, queued, in progress, needs validation, blocked, cancelled]
audience: programmer
breadcrumb: [Reference, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Autonomous Engineer plan and work item states

Plan and work item states appear during planning and execution. Identify where a plan or work item is in the execution process and what action is required.

## Plan states

The Autonomous Engineer dashboard displays the current state of the plan.

-   **Standby**

    The plan is not in progress. All work items are in Draft state.

-   **In progress**

    Autonomous Engineer is actively working on the plan. Work items are in progress or waiting.

-   **In review**

    Autonomous Engineer has completed all work. Work items are pending your review.

-   **Completed**

    The plan has been reviewed and completed and is ready for deployment.

-   **Cancelled**

    The plan was cancelled and will not be executed.


## Work item states

Each work item moves through states during plan execution. The plan dashboard displays the current state of every work item.

-   **Draft**

    The work item was generated during planning and has not yet been queued for execution.

-   **Ready**

    The work item has been reviewed and approved and is waiting for its dependencies to complete before it can be queued.

-   **Queued**

    The work item is in the execution queue and waits to be picked up by a background agent.

-   **Waiting**

    The work item has unmet dependencies and can't begin execution until those dependencies are complete.

-   **In progress**

    A background agent is actively building the work item.

-   **Needs validation**

    The work item is built and Automated Test Framework \(ATF\) tests have run. The work item requires your review before it can be marked complete.

-   **Complete**

    You have reviewed and approved the work item. Its artifacts are included in the plan update set.

-   **Blocked \(user input\)**

    The background agent requires information from you before it can continue. A notification appears in the chat panel.

-   **Blocked \(error\)**

    The background agent encountered an error it can't self-heal. Open the work item or ask Build Agent in the chat panel for details, then ask Build Agent to retry.

-   **Cancelled**

    The work item was cancelled and will not be executed. Cancelled work items aren't included in the plan update set.


**Parent Topic:**[Autonomous Engineer reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/autonomous-engineer-reference-landing.md)

