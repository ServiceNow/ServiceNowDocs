---
title: Opt-in for benchmark scores
description: Get benchmark scores by registering your instance to the ServiceNow central instance. The latter maintains information of multiple industries to provide the benchmark score.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-05"
reading_time_minutes: 1
keywords: [how to opt-in for benchmark scores]
breadcrumb: [Cybersecurity Executive Dashboard, Security Operations]
---

# Opt-in for benchmark scores

Get benchmark scores by registering your instance to the ServiceNow central instance. The latter maintains information of multiple industries to provide the benchmark score.

## Before you begin

Role required: admin

## About this task

For more information on Benchmarking, see [Exploring Benchmarks](https://www.servicenow.com/docs/access?context=exploring-benchmarks&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## Procedure

1.  To register your instance with the central instance, follow these steps:

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    2.  Select **sn\_bm\_client.central\_instance\_url** system property.

    3.  In the **Value** field, enter the benchmark central instance URL.

        **Note:** If the instance is provisioned, your details are pushed to the central instance automatically.

    4.  Select **Opt-in** from the widget to validate and establish a connection with the central instance.

2.  To upload your score to the central instance, follow these steps:

    1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**

    2.  Select the **Upload the benchmark scores** scheduled job.

    3.  Select **Update**.

        The scores are uploaded to the central instance. However, the scheduled jobs by the central instance run once a month to update the scores on the dashboard widgets.

3.  To download the score from the central instance, follow these steps:

    1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**

    2.  Select the **Download the benchmark scores** scheduled job.

    3.  Select **Execute Now**.

        The scores are available in the Benchmark Scores \[sn\_bm\_client\_score\_list\] table, which is reflected in the dashboard widgets.


