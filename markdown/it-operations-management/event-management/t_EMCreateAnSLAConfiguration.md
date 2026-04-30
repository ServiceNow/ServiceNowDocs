---
title: Create an SLA configuration for CIs
description: Create an SLA configuration from the Event Management application to determine which CIs are available for SLAs.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SLAs for application services and CIs, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Create an SLA configuration for CIs

Create an SLA configuration from the Event Management application to determine which CIs are available for SLAs.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The SLA configuration record is a filter on a table in the system. Select a table that has the CIs for which you want to create an SLA.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **SLA Configuration**.

2.  Click **New**.

3.  Fill in the form fields \(see table\).

    |Field|Description|
    |-----|-----------|
    |Name|Provide a descriptive name.|
    |Table|Select a table with the CIs for which you want to create the SLA. You can also use the Configuration Item to Host View \[query\_based\_service\_basic\_view\] table, which is used by [Dynamic CI Groups](https://www.servicenow.com/docs/access?context=create-it-services&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).|
    |Filter|Configure the filter for the records.|

4.  Right-click the header and select **Save**.


## Example

The following is an example.

If you want to run an SLA on all Linux servers for major and critical alerts, first create an SLA configuration on the Linux Server \[cmdb\_ci\_linux\_server\] table. Then create the SLA definition with this filter:

-   `CI.class` is `Linux Server`
-   `Severity` is `Major` or `Critical`

## What to do next

[Create an SLA definition](t_EMCreateSLADefForCI_BS.md) on the CIs that match this SLA configuration.

-   **[Limit the records for the SLA configuration filter](t_EMLimitTheRecordsForSLAConfigFilter.md)**  
If too many records are returned by the SLA configuration filter, you can add a property to set the maximum number of records.

**Parent Topic:**[SLAs for application services and CIs](../concept/c_EMSLAsForBSAndCIs.md)

