---
title: Add scenarios and review reference data
description: Select the adverse-event scenarios to test against the scoped service, then review the historical reference data that the system will use to auto-populate simulation inputs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-sca-scenarios-review-refdata.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Scenario Analysis, Operational Resilience, scenarios, reference data, Statistical Model Profile]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add scenarios and review reference data

Select the adverse-event scenarios to test against the scoped service, then review the historical reference data that the system will use to auto-populate simulation inputs.

## Before you begin

Role required: **sn\_oper\_res.admin**, **sn\_oper\_res.manager**

## About this task

The Scenarios step lets you select a scenario record. The Risk Events list in the Reference Data step is empty by default — no records are auto-populated; select **Add** to choose events.

**Note:** Selected records are captured as a snapshot; events created or updated after you mark the step complete are not reflected, and the snapshot does not refresh when the source risk-event record is updated.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and open the Scenario Analysis record form.

2.  In the Playbook stage panel, select **Scenarios**.

3.  Select **Add** to open the **Select Scenarios** dialog.

    \[Omitted image "sca-scenarios-step-empty.png"\] Alt text: The selected events define the disruptions tested in this analysis. Review carefully as these events can't be edited later, an empty 'Scenario analysis scenario' table, and the Add button enabled.

4.  Browse scenarios by **Name**, **Description**, or **Pillar**, then select one or more scenarios.

    If the scenario you need is not in the library, you can create a scenario directly from this window instead of navigating to the **All** menu.\[Omitted image "sca-scenarios-selection-dialog.png"\] Alt text: Scenario selection dialog with the row 'Flooding Situation' checked, columns Name, Description, and Pillars visible, and the Add button enabled.

5.  Select **Add** to confirm the selection.

    The **Scenarios** step shows a completed status in the stage panel. The action button shown on the **Reference Data** step is derived from the Statistical model profile selected on the record. Selecting the **Annual loss model driven by risk events** profile renders an **Add risk events** action; other profiles render the equivalent action for their reference table.

    \[Omitted image "sca-ref-data-add-risk-events.png"\] Alt text: Action button 'Add risk events' before risk events are added; the column headers are Risk Advanced Event, Scenario analysis, Expected loss, Net loss, Primary entity, Event type, and Sub type.\[Omitted image "sca-ref-data-risk-events-shown-per-selection.png"\] Alt text: Risk events selection dialog with five rows listed \(Employee information theft, Unauthorized marking down prices, and so on\) and columns Name, Primary entity, Event type, Sub type, and State. \[Omitted image "sca-ref-data-filter-applied.png"\] Alt text: Risk events selection dialog with a filter applied, the Run button enabled, and the filtered result rows ready for selection.\[Omitted image "sca-ref-data-risk-events-added.png"\] Alt text: Risk events selection dialog with two rows checked \('Unauthorized marking down prices…' and 'Disputes related to the improper conclusion and developments contracts…'\) and the Add button enabled.

6.  Select **Mark as complete**.

    The Scenarios step is complete.

7.  Select **Reference Data** in the Playbook stage panel.

8.  To open the risk event selection pop-up, select **Add** in the Risk Events section.

    The pop-up lists all available risk events with the columns **Name**, **Primary entity**, **Event type**, **Sub type**, and **State** by default. Use the **Add condition** control to filter by other attributes \(for example, **Date of discovery** or **Net loss**\) before confirming a selection.

    \[Omitted image "sca-reference-data-popup-risk-events.png"\] Alt text: Add risk events pop-up showing the paginated list with the default columns Name, Primary entity, Event type, Sub type, and State.

    You can associate reference data with the scope and add tags and descriptions.

9.  Select the checkboxes for the desired risk events, then confirm.

    The selected risk events appear in the Risk Events list on the **Reference Data** step.

10. Verify that the listed events are appropriate for the service in scope, then select **Mark as complete**.

    The **Reference Data** step shows a completed status in the stage panel.

    \[Omitted image "sca-ref-data-complete.png"\] Alt text: Reference data complete.


## Result

The **Scenarios** and **Reference Data** steps are complete. The playbook advances to **Scenario Testing**.

## What to do next

For information on completing scenario testing, see [Start simulation and run scenario testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-scenario-testing.md).

