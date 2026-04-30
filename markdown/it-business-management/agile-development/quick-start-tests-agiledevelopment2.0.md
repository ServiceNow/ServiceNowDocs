---
title: Quick start tests for Agile Development 2.0
description: Validate that Agile Development 2.0 still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: zurich
product: Agile Development
classification: agile-development
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Quick start tests for Agile Development 2.0

Validate that Agile Development 2.0 still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Agile Development 2.0 quick start tests require activating the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) and the Agile Development 2.0 - ATF Tests plugin \(com.snc.sdlc.agile.2.0.atf \).

<table id="atf-tests-Agile2.0"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

Verify that global rank is populated when a story is created

</td><td>

Verify the global rank of a story after creation.

</td><td>

Madrid

</td></tr><tr><td>

Verify that closing a sprint with active stories is prevented

</td><td>

Verify that a sprint with active stories cannot be closed.

</td><td>

Madrid

</td></tr><tr><td>

Verify that sprints cannot overlap in the same group

</td><td>

Verify that sprints in the same group do not overlap.

</td><td>

Madrid

</td></tr><tr><td>

Verify that sprint points are updated

</td><td>

Verify that changes to stories produce accurate sprint point totals.

</td><td>

Madrid

</td></tr><tr><td>

Verify that only one sprint in a group can have the current state

</td><td>

Verify sprint statuses.

</td><td>

Madrid

</td></tr><tr><td>

Verify sprint end date is after the sprint start date

</td><td>

Verify sprint start and end dates.

</td><td>

Madrid

</td></tr><tr><td>

Verify that any update on story rolls up to Epic

</td><td>

Verify that adding, estimating, removing, deleting, updating, or cancelling a story updates the epic-level roll-ups correctly.

</td><td>

Orlando

</td></tr><tr><td>

Verify changes to the scope of a current sprint do not alter the value of the Total Committed Points

</td><td>

Verify that the value of Total Committed Points does not change with change in the scope of a sprint after its state is changed to Current.

</td><td>

Orlando

</td></tr><tr><td>

Verify active flag is set false when Agile Story state is changed to Completed/Cancelled

</td><td>

Verify that active flag of an Agile story is set to the following: -   False, if the state is changed to Completed or Cancelled
-   True, for all other states

</td><td>

Orlando

</td></tr><tr><td>

Verify that updating the team/group capacity overrides the capacity on all the future sprints

</td><td>

Verify that any update to the **Group capacity** field of the assignment group results in the following changes to the **Group capacity** field of the various sprints associated with this assignment group:

-   For the sprints that are in the Draft and Planning state:
    -   The group capacity is updated to the new value.
    -   The **Group capacity** field is editable.
-   For the sprints in the Current, Complete, or Cancelled state:
    -   The group capacity remains the old value.
    -   The **Group capacity** field is read-only.

 For the sprints in the Draft or Planning state, you can individually edit the group capacity of the sprint anytime later. This would not change the group capacity of the assignment group associated with this sprint.

</td><td>

Paris

</td></tr><tr><td>

Verify create and edit functionality of an epic backlog on the scrum program board

</td><td>

-   Verify that you can create an epic backlog for scrum programs from the Backlog tab of Agile Board.
-   Verify that you can update an existing epic backlog for scrum programs from the Backlog tab of Agile Board.
-   The epics listed in the backlog must belong to the selected epic backlog.

</td><td>

Quebec

</td></tr><tr><td>

Verify a Demand is converted to a scrum story

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to an Agile 2.0 story using the **Create Story** related link on the Demand form. For more information on how to create an Agile 2.0 story from a demand, see [Create an artifact from a demand](../../../product/planning-and-policy/task/t_CrtArtftDmdMnu.md).

</td><td>

Quebec

</td></tr><tr><td>

Verify a Demand is converted to a scrum epic

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to an Agile 2.0 epic using the **Create Epic** related link on the Demand form.For more information on how to create an Agile 2.0 epic from a demand, see [Create an artifact from a demand](../../../product/planning-and-policy/task/t_CrtArtftDmdMnu.md).

</td><td>

Quebec

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Agile Development 2.0](../../../product/agile-development/concept/setting-up-agile-development-2.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

