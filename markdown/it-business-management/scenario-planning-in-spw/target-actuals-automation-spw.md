---
title: Target actuals automation in Strategic Planning
description: Automate the actual value for your targets using the target automation feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/scenario-planning-in-spw/target-actuals-automation-spw.html
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 2
breadcrumb: [Manage portfolio plan goals, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Target actuals automation in Strategic Planning

Automate the actual value for your targets using the target automation feature.

target actuals automation in strategic planning 

Use the following steps as guidelines to enable actuals automation and configure a target source for a target using the target automation feature.

You must perform the following steps on the [Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/target-form-egm.md) to enable target automation for the target.

1.  Enter the Start value, Final target value, and Check-in frequency, and fill the other required fields for the target.
2.  Select the **Automate actual value** field.

    \[Omitted image "target-automation-enabling.png"\] Alt text: Enabling target automation in Strategic Planning

3.  Select a target source in the **Actual value source** field, from which the value must be fetched for target automation.

    A target source is a configuration \(of a custom script, PA indicator, or Assessments\) for a target to auto-update the actual value of the target, so that the progress of the target and its goal are auto-updated.

    \[Omitted image "target-automation-selecting-target-source.png"\] Alt text: Selecting target source for automating target actuals in Strategic Planning

    You can select either the Benefit Plans option or a custom target source as a target source for the target. After selecting a target source, save the target record to view additional actual value source configuration.

    -   Benefit Plans target source - A target source that is created using a custom script where the actual benefit value of benefit plans of the planning items associated with the goal or target fetches the target actuals. Then the application updates the actual value of the target based on the actual benefit value.

        When you select Benefit Plans target source \([predefined target automation script for benefit plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/target-automation-script-benefit-plans-apw.md)\) as the Actual value source for the target, the **benefit\_plan** field appears in the Variables section, from which you can select the required benefit plans for fetching the value and automating the actual value of the target.

        **Note:** Only benefit plans of the planning items associated with the goal or target will be available to select in the **benefit\_plan** field as a source for target automation.

        \[Omitted image "target-automation-selecting-benefit-plan.png"\] Alt text: Benefit plan variables for target source in Strategic Planning

    -   Custom target source - Create a custom target source and configure it as a source to update the actual value of the target. For instructions on how to create a target source, see [Create a target source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/create-target-source-for-automating-the-actual-value-of-the-targets-apw.md).
    For instructions on creating targets for a goal, see [Add targets for a goal in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/set-targets-for-goal-egm.md).


