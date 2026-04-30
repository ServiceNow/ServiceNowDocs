---
title: Set improvement opportunities
description: Set improvement opportunities to find areas of improvement by which teams could optimize a process. You can either select from a list of rules available to you or set your own rules. Based on the rules set by you, you can view your areas of improvement.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Set improvement opportunities

Set improvement opportunities to find areas of improvement by which teams could optimize a process. You can either select from a list of rules available to you or set your own rules. Based on the rules set by you, you can view your areas of improvement.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## About this task

There are two types of improvement opportunities that could be set up:

-   Rule-based improvement opportunities: These improvement opportunities consist of one or more finding rule chains executed in a sequence. The records that match the logic of these specifications are classified as a match for the improvement opportunities.

-   Automated improvement opportunities: The improvement opportunities are displayed based on the default patterns that are already available for selection.


## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Scope your analysis** page, select the **Set improvement opportunities** tab.

2.  Select **Edit** for the project that you want to edit.

3.  Select the edit button for the **Improvement opportunities** section.

4.  On the **Select improvement opportunities** tab, select **New**.

    The Improvement opportunity definition page is displayed. This page displays all the improvement opportunities definitions that are available. You can find the definition of each improvement opportunity along with an illustration and example.

    ![Improvement opportunity definition](../image/imp-opp-def.png)

5.  Select **Create** on any of the cards to create an improvement opportunity of that type.

    For more information on rule-based improvement opportunity, see [Set rule-based improvement opportunity](rule-based-builder.md).

    For more information on automated improvement opportunity, see [Automated improvement opportunities](../concept/automated-findings.md).

6.  To edit an improvement opportunity, select the improvement opportunity and edit the details.

7.  To delete an improvement opportunity, select the finding definition, and then select **Delete**.

8.  To select an improvement opportunity from the library, select **Add from library**, and then select an improvement opportunity.

    These rules are available from the table configuration. If there are improvement opportunities configured for the table you have selected for your project, then you see those findings in the library. For information about table configuration, see [Create process configuration record for the table](create-process-config.md).

9.  Select **Review and mine**.


**Parent Topic:**[Create a project or template using Project Builder](define-workflow-model.md)

