---
title: Plan overview scorecards for plan usage details
description: The Overview tab gives you the details of the plan and the exercise and actual events that use the plan. It also indicates how successful the plan was in recovering the assets in a loss scenario.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [View plan details, Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# Plan overview scorecards for plan usage details

The **Overview** tab gives you the details of the plan and the exercise and actual events that use the plan. It also indicates how successful the plan was in recovering the assets in a loss scenario.

## Plan usage and results

The Plan Usage and Results section shows the details of the crisis and exercise events that use the current plan that you are viewing.

-   **Related Crisis Events**

    -   Total Crisis Events: The total number of crisis events that use the current plan.
    -   Ongoing Crisis Events: The number of crisis events that are currently in progress.
    -   Last Crisis Event Date: The actual end date and time of the last crisis event that happened.
    ![Related crisis events of the plan](../image/RelatedCrisisEventsScorecard.png "Related crisis events")

-   **Related Exercises**

    -   Total Exercises: The total number of exercises that use the current plan.
    -   Ongoing Exercises: The number of exercise events that are currently in progress.
    -   Last Exercise Date: The actual end date and time of the last completed exercise event.
    -   Last Exercise Result: Indicates whether the last completed exercise event was successful or not.
    ![Related exercises with date and time](../image/RelatedExercisesScorecard.png "Related exercises")

-   **Exercise Results**

    The color-coded donut indicates the number of completed exercise events that were successful, unsuccessful, and successful with issues.

    ![Exercise results](../image/ExerciseResultsDonut.png "Exercise results")


## Plan details

-   **Scope**

    Displays all the assets identified in the plan as **Total**. Out of all the RPO and RTO that a primary element supports, the minimum value of RPO and RTO is displayed.

    ![Plan assets scorecard](../image/PlanAssetsScorecard.png "Plan assets scorecard")

-   **Recovery Teams**

    The scorecard helps you to identify teams and individuals with clear guidelines of responsibilities to act at the time of a crisis.

    The assigned score indicates that a recovery role of a plan has been assigned to a group or a user. The unassigned score indicates that the recovery role is not assigned to any group or user.

    ![Recovery team widget](../image/RecoveryWidget.png "Recovery teams scorecard")

-   **Documentation**

    Displays the total number of documentation sections that are attached to the plan. The breakdown shows the status of the documentation sections that are updated according to the plan and in **Complete** state. The **Pending** state indicates the documentation sections that are still under edit.

    ![Documentation scorecard](../image/DocumentationSectionWidget.png "Documentation scorecard")

-   **Recovery Tasks**

    The recovery tasks scorecard indicates a group and an owner for the group, identified to carry out the activities of the plan during the recovery process.

    ![Activities scorecard](../image/ActivitiesScoreWidget.png "Recovery Tasks scorecard")

    Out of the total number of activities identified for the plan, the assigned score indicates the number of activities for which groups have been assigned. Unassigned score indicates plan activities for which groups have not been assigned.

-   **Dependencies by Loss scenario**

    The donut chart shows the assets covered by a strategy, and uses colors to indicate whether the asset has a strategy or not. A loss scenario plan must have at least one strategy for an asset. However, you can also have a single strategy covering multiple assets.

    ![Dependencies by loss scenarios](../image/DependenciesByLS.png "Dependencies by loss scenarios")


**Parent Topic:**[View plan details in scorecards](../task/view-bcp-scorecard.md)

