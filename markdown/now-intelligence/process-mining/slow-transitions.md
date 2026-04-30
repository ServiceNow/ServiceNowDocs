---
title: Configure slow transitions
description: Configure a slow transitions finding definition to view a pattern where clusters of records have an unusual duration that's higher than the average duration of another group of records.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automated improvement opportunities, Setting improvement opportunity from Project Builder, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure slow transitions

Configure a slow transitions finding definition to view a pattern where clusters of records have an unusual duration that's higher than the average duration of another group of records.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

Slow transitions finding definition displays clusters of records that have an unusual duration that's higher than the average duration of another group of records. This helps identify slower progression for a significant group of records.

![Slow transition](../image/slow-transition.png)

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about the Improvement opportunity definition page, see [Set improvement opportunities](improve-opportunities.md).

2.  Select **Create** on the Slow transition card.

    For a particular type of automated finding, you can create a maximum of two automated findings.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form from Finding Builder](../reference/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

5.  Fill the details on the form.

    Default values are provided. You can edit them if needed.

    ![Slow transition configuration](../image/slow-transition-config.png)

    According to the example, records that meet the following conditions are available as improvement opportunities in the Summary and Insights page:

    -   The transition should have at least 50 occurrences with a minimum of 20 slow transitions and 20 regular transitions.
    -   The difference between the shortest transition in the slow transition group and the longest transition in the regular transition group must be at least 120 minutes.
    -   Only the top five slow transitions are displayed in the Summary and Insights page.
6.  Select **Save and exit**.


**Parent Topic:**[Automated improvement opportunities](../concept/automated-findings.md)

