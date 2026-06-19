---
title: Plan overview scorecards for plan usage details
description: The Overview tab gives you the details of the plan and the exercise and actual events that use the plan. It also indicates how successful the plan was in recovering the assets in a loss scenario.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/plan-overview-scorecards.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View plan details, Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Plan overview scorecards for plan usage details

The **Overview** tab gives you the details of the plan and the exercise and actual events that use the plan. It also indicates how successful the plan was in recovering the assets in a loss scenario.

## Plan usage and results

The Plan Usage and Results section shows the details of the crisis and exercise events that use the current plan that you are viewing.

-   **Related Crisis Events**

    -   Total Crisis Events: The total number of crisis events that use the current plan.
    -   Ongoing Crisis Events: The number of crisis events that are currently in progress.
    -   Last Crisis Event Date: The actual end date and time of the last crisis event that happened.
    \[Omitted image "RelatedCrisisEventsScorecard.png"\] Alt text: Related crisis events of the plan

-   **Related Exercises**

    -   Total Exercises: The total number of exercises that use the current plan.
    -   Ongoing Exercises: The number of exercise events that are currently in progress.
    -   Last Exercise Date: The actual end date and time of the last completed exercise event.
    -   Last Exercise Result: Indicates whether the last completed exercise event was successful or not.
    \[Omitted image "RelatedExercisesScorecard.png"\] Alt text: Related exercises with date and time

-   **Exercise Results**

    The color-coded donut indicates the number of completed exercise events that were successful, unsuccessful, and successful with issues.

    \[Omitted image "ExerciseResultsDonut.png"\] Alt text: Exercise results


## Plan details

-   **Scope**

    Displays all the assets identified in the plan as **Total**. Out of all the RPO and RTO that a primary element supports, the minimum value of RPO and RTO is displayed.

    \[Omitted image "PlanAssetsScorecard.png"\] Alt text: Plan assets scorecard

-   **Recovery Teams**

    The scorecard helps you to identify teams and individuals with clear guidelines of responsibilities to act at the time of a crisis. The assigned score indicates that a recovery role of a plan has been assigned to a group or a user. The unassigned score indicates that the recovery role is not assigned to any group or user.

    \[Omitted image "RecoveryWidget.png"\] Alt text: Recovery team widget

-   **Documentation**

    Displays the total number of documentation sections that are attached to the plan. The breakdown shows the status of the documentation sections that are updated according to the plan and in **Complete** state. The **Pending** state indicates the documentation sections that are still under edit.

    \[Omitted image "DocumentationSectionWidget.png"\] Alt text: Documentation scorecard

-   **Recovery Tasks**

    The recovery tasks scorecard indicates a group and an owner for the group, identified to carry out the activities of the plan during the recovery process. Out of the total number of activities identified for the plan, the assigned score indicates the number of activities for which groups have been assigned. Unassigned score indicates plan activities for which groups have not been assigned.

    \[Omitted image "ActivitiesScoreWidget.png"\] Alt text: Activities scorecard

-   **Dependencies by Loss scenario**

    The donut chart shows the assets covered by a strategy, and uses colors to indicate whether the asset has a strategy or not. A loss scenario plan must have at least one strategy for an asset. However, you can also have a single strategy covering multiple assets.

    \[Omitted image "DependenciesByLS.png"\] Alt text: Dependencies by loss scenarios


