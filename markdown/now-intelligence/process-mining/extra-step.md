---
title: Configure extra step finding definition
description: Configure an extra-step finding definition to view a pattern where routes differ by one additional step.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automated improvement opportunities, Setting improvement opportunity from Project Builder, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure extra step finding definition

Configure an extra-step finding definition to view a pattern where routes differ by one additional step.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

Extra-step finding definition surfaces variants \(routes\) in the process that differ by only one additional step, which could possibly be automated or eliminated to save time.

![Extra step](../image/extra-step.png)

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about Improvement opportunity definition page, see [Set improvement opportunities](improve-opportunities.md).

2.  Select **Create** on the Extra step card.

    For a particular type of automated finding, you can create a maximum of two automated findings.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form from Finding Builder](../reference/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

5.  Fill the details on the form.

    Default values are provided. You can edit them if needed.

    ![Extra step configuration](../image/extra-step-config.png)

    According to the example, records that meet the following conditions are available as improvement opportunities in the Summary and Insights page:

    -   Checks for variants \(routes\) with a minimum of 7 steps to find similar variants with an extra step. The steps include **Process start** and **Process end**. Also, the variants must have a minimum of 10 records.
    -   Only variants with 20% to 100% of the of the volume of the efficient route will be considered. However, variants with 100 records will always be considered irrespective of the percentage.
    -   Only top 10 variants will be displayed in the Summary and Insights page.
6.  Select **Save and exit**.


**Parent Topic:**[Automated improvement opportunities](../concept/automated-findings.md)

