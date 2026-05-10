---
title: Quick start tests for Essential SAFe
description: Validate that Essential SAFe still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Quick start tests for Essential SAFe

Validate that Essential SAFe still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Essential SAFe quick start tests require activating the Agile - Scaled Agile Framework - Essential SAFe plugin \(com.snc.sdlc.safe\) and the Agile - Scaled Agile Framework - Essential SAFe - ATF Tests plugin \(com.snc.sdlc.safe.atf\).

<table id="table_vqt_4nd_vfb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

Essential SAFe: Feature tests

</td><td>

Verify feature global rank updates.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Feature tests

</td><td>

For a SAFe feature, verify that:

-   Actual start date is populated after the state is changed to Implementation, Validation on Staging, or Deployment.
-   Actual end date is populated after the state is changed to **Released** or **Cancelled**.
-   Active flag is set to the appropriate value:
    -   **False**, if the state is changed to **Released** or **Cancelled**.
    -   **True**, for all other states.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Feature tests

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to a SAFe feature using the **Create SAFe Feature** related link on the Demand form. For more information on how to create an SAFe feature from a demand, see [Create an artifact from a demand](../../../product/planning-and-policy/task/t_CrtArtftDmdMnu.md).

</td><td>

Quebec

</td></tr><tr><td>

Essential SAFe: Program increment tests

</td><td>

Verify program increment date overlapping.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Sprint tests

</td><td>

Verify the generation of ART sprints and team sprints as well as updates to sprint points and dates.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Sprint tests

</td><td>

Verify that any update to the **Group capacity** field of the assignment group results in the following changes to the **Group capacity** field of the various sprints associated with this assignment group:

-   For the sprints that are in the **Draft** or **Planning** states:
    -   The group capacity is updated to the new value.
    -   The **Group capacity** field is editable.
-   For the sprints in the **Current**, **Complete**, or **Cancelled** states:
    -   The group capacity remains the old value.
    -   The **Group capacity** field is read-only.

 For the sprints in the **Draft** or **Planning** state, you can individually edit the group capacity of the sprint anytime later. This would not change the group capacity of the assignment group associated with this sprint.

</td><td>

Paris

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify story global rank updates.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify that active flag of the SAFe story is set to the appropriate value:

-   **False**, if the state of the state is changed to Completed or Cancelled.
-   True, for all other states.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify that adding, estimating, removing, deleting, updating, or cancelling a SAFe story updates the SAFe feature-level and then the epic-level roll-ups correctly.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify that adding, updating, or deleting the feature on a SAFe story updates the Epic field on the SAFe story form.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to a SAFe story using the **Create SAFe Story** related link on the Demand form. For more information on how to create a SAFe story from a demand, see [Create an artifact from a demand](../../../product/planning-and-policy/task/t_CrtArtftDmdMnu.md).

</td><td>

Quebec

</td></tr><tr><td>

Essential SAFe: Team tests

</td><td>

Verify team association with an ART.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Epic tests

</td><td>

For a SAFe epic, verify that:-   Actual start date is populated after the state is changed to **Implementation**.
-   Actual end date is populated after the state is changed to **Complete**.
-   Active flag is set to the appropriate value:
    -   **False**, if the state is changed to **Released** or **Cancelled** states.
    -   **True**, for all other states.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Epic tests

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to a SAFe epic using the **Create SAFe Epic** related link on the Demand form.For more information on how to create a SAFe epic agile from a demand, see [Create an artifact from a demand](../../../product/planning-and-policy/task/t_CrtArtftDmdMnu.md).

</td><td>

Quebec

</td></tr><tr><td>

Essential SAFe: Program PI Objective tests

</td><td>

Verify the functionality of creating and updating PI objectives-   Verify that you can create a program increment-level objective
-   Verify that you can update the created PI objective with the planned business value \(PBV\) and actual business value \(ABV\)
-   Verify that the percentage of business value achieved is computed as the percentage of ABV complete, for only the committed PI objectives, as compared to the PBV of the program in the PI

</td><td>

Rome

</td></tr><tr><td>

Essential SAFe: Team PI Objective tests

</td><td>

Verify the functionality of creating and updating team PI Objectives-   Verify that you can create a team-level PI objective
-   Verify that you can update the created PI objective with the planned business value \(PBV\) and actual business value \(ABV\)
-   Verify that the percentage of business value achieved is computed as the percentage of ABV complete, for only the committed PI objectives, as compared to the PBV of the team in the PI

</td><td>

Rome

</td></tr></tbody>
</table>**Parent Topic:**[Essential SAFe](../../../product/agile-SAFe/concept/essential-overview.md)

**Related topics**  


[Components installed with Essential SAFe](../../../product/agile-SAFe/reference/installed-with-EssentialSAFe.md)

[SAFe entities](../../../product/agile-SAFe/concept/key-entities-SAFe.md)

[SAFe PI objectives](../../../product/agile-SAFe/concept/safe-pi-objectives.md)

[SAFe Board — ART level](../../../product/agile-SAFe/concept/program-level-tabs.md)

[SAFe Board — Team level](../../../product/agile-SAFe/concept/team-level-tabs.md)

[Quick start tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/quick-start-tests.md)

