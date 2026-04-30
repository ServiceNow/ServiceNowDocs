---
title: Configure the Google Cloud Platform \(GCP\) configuration data file
description: Configure the Google Cloud Platform \(GCP\) configuration data file to monitor metrics in your GCP environment.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Configure the Google Cloud Platform \(GCP\) configuration data file

Configure the Google Cloud Platform \(GCP\) configuration data file to monitor metrics in your GCP environment.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

The GCP configuration data file is a .json file which contains all of the metrics collected from your GCP environment. Metrics that you add to the **acc\_gcp\_metrics\_list.json** file are monitored by the check to which the file is attached.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Configuration Files**.

2.  Locate the **acc\_gcp\_metrics\_list.json** configuration file.

3.  Download and add the GCP metrics to the configuration file that you want to be monitored.

    For details on the available GCP metrics, see [Google Cloud Platform \(GCP\) metrics](../reference/gcp-metrics.md).

4.  Select the Manage Attachments icon \(![](../image/paper-clip-icon.png)\) to attach the updated configuration file.


**Parent Topic:**[Agent Client Collector deployment - shared between servers and endpoints](../concept/acc-shared-deployment.md)

