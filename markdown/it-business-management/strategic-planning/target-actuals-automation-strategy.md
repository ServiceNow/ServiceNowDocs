---
title: Target actuals automation
description: Automate the actual value for your targets using the target automation feature.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Manage enterprise goals, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Target actuals automation

Automate the actual value for your targets using the target automation feature.

Use the following steps as guidelines to enable actuals automation and configure a target source for a target using the target automation feature.

You must perform the following steps on the [Target form](../../spw-goals/reference/target-form-egm.md) to enable target automation for the target.

1.  Enter the Start value, Final target value, and Check-in frequency, and fill the other required fields for the target.
2.  Select the **Automate actual value** field.

    ![Enabling target automation in Strategic Planning](../image/target-automation-enabling-strategy.png)

3.  Select a target source in the **Actual value source** field, from which the value must be fetched for target automation.

    A target source is a configuration \(of a custom script, PA indicator, or Assessments\) for a target to auto-update the actual value of the target, so that the progress of the target and its goal are auto-updated.

    ![Selecting target source for automating target actuals in Strategic Planning](../image/target-aitomation-selecting-target-source-strategy.png)

    You can select either the Benefit Plans option or a custom target source as a target source for the target. After selecting a target source, save the target record to view additional actual value source configuration.

    -   Benefit Plans target source - A target source that is created using a custom script where the actual benefit value of benefit plans of the planning items associated with the goal or target fetches the target actuals. Then the application updates the actual value of the target based on the actual benefit value.

        When you select Benefit Plans target source \([predefined target automation script for benefit plans](../../spw-goals/reference/target-automation-script-benefit-plans-apw.md)\) as the Actual value source for the target, the **benefit\_plan** field appears in the Variables section, from which you can select the required benefit plans for fetching the value and automating the actual value of the target.

        **Note:** Only benefit plans of the planning items associated with the goal or target will be available to select in the **benefit\_plan** field as a source for target automation.

        ![Benefit plan variables for target source in Strategic Planning](../image/target-aitomation-selecting-benefit-plan-strategy.png)

    -   Custom target source - Create a custom target source and configure it as a source to update the actual value of the target. For instructions on how to create a target source, see [Create a target source](../../spw-goals/task/create-target-source-for-automating-the-actual-value-of-the-targets-apw.md).
    For instructions on creating targets for a goal, see [Add a target for goal](../task/set-target-for-goal-strategy.md).


**Related topics**  


[Create a goal](../task/create-goal-strategy.md)

[Add a target for goal](../task/set-target-for-goal-strategy.md)

[Duplicate a goal or target](../task/duplicate-goal-target-strategy.md)

[Send a reminder for target actuals check in](../task/send-reminder-target-checkin-strategy.md)

