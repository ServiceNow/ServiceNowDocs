---
title: Configure extreme repetitions finding definition
description: Configure an extreme repetitions finding definition to view a pattern where a transition repeats more than the usual repetition range between the steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/extreme-repetitions.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated improvement opportunities, Setting improvement opportunity from Project Builder, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure extreme repetitions finding definition

Configure an extreme repetitions finding definition to view a pattern where a transition repeats more than the usual repetition range between the steps.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

Extreme repetitions finding definition surfaces transitions that are repeated significantly more than the median repetition. This helps uncover potential repetition anomalies.

\[Omitted image "extreme-repetition.png"\] Alt text: Extreme repetition

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about the Improvement opportunity definition page, see [Set improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/improve-opportunities.md).

2.  Select **Create** on the Extreme repetitions card.

    For a particular type of automated finding, you can create a maximum of two automated findings.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form from Finding Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

5.  Fill the details on the form.

    Default values are provided. You can edit them if needed.

    \[Omitted image "extreme-repetition-config.png"\] Alt text: Extreme repetition configuration

    According to the example, records that meet the following conditions are available as improvement opportunities in the Summary and insights page:

    -   Records that take the minimum time, which is the number of times specified multiplied by the median duration. In the example, it is 20\*median duration.
    -   Only 2% of the total records are included so that a large number of records aren’t displayed. Also, a minimum of 20 records is considered.
    -   Only the top five extreme duration transitions are displayed in the Summary and insights page as improvement opportunities.
6.  Select **Save and exit**.


**Parent Topic:**[Automated improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/automated-findings.md)

