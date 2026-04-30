---
title: Input parameters for Remedial action in Proactive Engagement
description: Additional input parameters are listed based on the type of remedial action chosen. Advanced settings for each of those input parameters list the information of the input parameters of the selected remedial action.
locale: en-US
release: xanadu
product: Proactive Engagement
classification: proactive-engagement
topic_type: reference
last_updated: "2025-04-02"
reading_time_minutes: 1
breadcrumb: [Proactive Engagement reference, Proactive Engagement, IT Service Management]
---

# Input parameters for Remedial action in Proactive Engagement

Additional input parameters are listed based on the type of remedial action chosen. Advanced settings for each of those input parameters list the information of the input parameters of the selected remedial action.

Depending on the remedial action chosen from the list, specific input parameters are listed which will fetch a static input. To fetch data from the table, enable and configure the advanced settings of the input parameters to capture the data during the run time. Find below the details of all the advanced settings of one of the out-of-the-box remedial action input parameters for Clear application cache. On saving the resolution, we should save parameter information in the `sn_pren_resolution table` remedial\_action\_parameters field

![Advanced settings for input parameters](../images/ra-advset1.png)

|Input parameter|Description|
|---------------|-----------|
|App name|Name of the application for clearing cache.|
|Process name|Name of the process that needs to be shut down.|
|Cache path|Folder path to clear the cache files of the specific application.|

Only text, boolean, or choice are the supported format for the input parameters. The Boolean format do not have the advanced configuration option.

**Note:** Check the alert action of Proactive Engagement to configure the input parameters. Currently, input parameters for remedial action cannot be configured from the Proactive Engagement workbench or the Core UI.

**Parent Topic:**[Proactive Engagement reference](../proactive-engagement-reference.md)

