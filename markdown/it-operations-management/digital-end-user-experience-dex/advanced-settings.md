---
title: Input parameters for remedial actions in Proactive Engagement
description: Remedial actions display input parameters based on the selected remedial action. Advanced settings for each input parameter define how the parameter captures data at run time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/advanced-settings.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Reference, Digital End-User Experience, IT Operations Management]
---

# Input parameters for remedial actions in Proactive Engagement

Remedial actions display input parameters based on the selected remedial action. Advanced settings for each input parameter define how the parameter captures data at run time.

Depending on the remedial action chosen from the list, specific input parameters are listed that fetch a static input. To fetch data from the table, turn on and configure the advanced settings of the input parameters to capture the data during the run time. The following table lists the advanced settings of the input parameters for the base system Clear application cache remedial action. When you save the resolution, the parameter information is saved in the remedial\_action\_parameters field of the `sn_pren_resolution table`.

\[Omitted image "ra-advset1.png"\] Alt text: Advanced settings for input parameters

|Input parameter|Description|
|---------------|-----------|
|App name|Name of the application for clearing cache.|
|Process name|Name of the process that needs to be shut down.|
|Cache path|Folder path to clear the cache files of the specific application.|

The supported formats for input parameters are text, Boolean, and choice. The Boolean format doesn't have the advanced configuration option.

**Note:** Configure the input parameters in the Proactive Engagement alert action. Input parameters for remedial actions can't be configured from the Proactive Engagement workbench or the Core UI.

