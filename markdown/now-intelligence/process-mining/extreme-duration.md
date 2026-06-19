---
title: Configure extreme duration finding definition
description: Configure an extreme duration finding definition to view a pattern where transitions take significantly longer than the usual duration between the steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/extreme-duration.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated improvement opportunities, Setting improvement opportunity from Project Builder, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure extreme duration finding definition

Configure an extreme duration finding definition to view a pattern where transitions take significantly longer than the usual duration between the steps.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

Extreme duration finding definition displays transitions that take significantly longer than the median duration. This helps uncover potential duration anomalies.

\[Omitted image "extreme-duration.png"\] Alt text: Extreme duration

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about the Improvement opportunity definition page, see [Set improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/improve-opportunities.md).

2.  Select **Create** on the Extreme duration card.

    For a particular type of automated finding, you can create a maximum of two automated findings.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form from Finding Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

5.  Fill the details on the form.

    Default values are provided. You can edit them if needed.

    \[Omitted image "extreme-duration-config.png"\] Alt text: Extreme duration configuration

    According to the example, records that meet the following conditions are available as improvement opportunities in the Summary and insights page:

    -   Records that take the minimum time, which is the number of times specified multiplied by the median duration.
    -   Only 2% of the total records will be included so that a large number of records are not displayed. Also, a minimum of 20 records will be considered.
    -   Only the top five extreme duration transitions are displayed in the Summary and insights page.
6.  Select **Save and exit**.


**Parent Topic:**[Automated improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/automated-findings.md)

