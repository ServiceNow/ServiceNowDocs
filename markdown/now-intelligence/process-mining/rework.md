---
title: Configure rework finding definition
description: Configure a rework finding definition to view a pattern where a step in the process is repeated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/rework.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated improvement opportunities, Setting improvement opportunity from Project Builder, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure rework finding definition

Configure a rework finding definition to view a pattern where a step in the process is repeated.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

Rework finding definition displays repeated process steps. This helps in identifying situations where there could be frequent repetition of work.

\[Omitted image "rework.png"\] Alt text: Rework

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about the Improvement opportunity definition page, see [Set improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/improve-opportunities.md).

2.  Select **Create** on the rework card.

    For a particular type of automated finding, you can create a maximum of two automated findings.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form from Finding Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

5.  Fill the details on the form.

    Default values are provided. You can edit them if needed.

    \[Omitted image "rework-configure.png"\] Alt text: Rework configuration

    According to the example, records that meet the following conditions are available as improvement opportunities in the Summary and insights page:

    -   A record in which one step is repeated more than 2 times.
    -   Only the top 10 records are displayed in the Summary and insights page.
6.  Select **Save and exit**.


**Parent Topic:**[Automated improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/automated-findings.md)

