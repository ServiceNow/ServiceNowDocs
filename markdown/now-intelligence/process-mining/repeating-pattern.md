---
title: Configure repeating pattern finding definition
description: Configure a repeating pattern finding definition to view a pattern with a series of repeating sequence of steps.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automated improvement opportunities, Setting improvement opportunity from Project Builder, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure repeating pattern finding definition

Configure a repeating pattern finding definition to view a pattern with a series of repeating sequence of steps.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

Repeating pattern finding definition displays the repetition of a specific order of steps. This brings the focus to the areas where you want to improve or automate certain parts or the process that are revisited.

![Repeating patterns](../image/repeating-patterns.png)

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about the Improvement opportunity definition page, see [Set improvement opportunities](improve-opportunities.md).

2.  Select **Create** on the Repeating pattern card.

    For a particular type of automated finding, you can create a maximum of two automated findings.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form from Finding Builder](../reference/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

5.  Fill the details on the form.

    Default values are provided. You can edit them if needed.

    ![Repeating patterns configuration](../image/repeating-patterns-config.png)

    According to the example, records that meet the following conditions will be available as improvement opportunities in the Summary and Insights page:

    -   A record must be repeated at least 2 times.
    -   The repeating pattern must have at least 3 steps.
    -   Only the top 5 repeated patterns are displayed in the Summary and Insights page.
6.  Select **Save and exit**.


**Parent Topic:**[Automated improvement opportunities](../concept/automated-findings.md)

