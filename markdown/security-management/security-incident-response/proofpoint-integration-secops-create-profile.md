---
title: Create an event profile for the Proofpoint Integration for Security Operations
description: Create an event profile to identify the events you want to import from the Proofpoint product.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-17"
reading_time_minutes: 2
breadcrumb: [Configuring the Proofpoint Integration for Security Operations, Proofpoint Integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an event profile for the Proofpoint Integration for Security Operations

Create an event profile to identify the events you want to import from the Proofpoint product.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  Navigate to **All** &gt; **SIR Integration with Proofpoint** &gt; **Proofpoint Events Profile**.

2.  Select **New**.

3.  Fill in the fields.

    The progress bar is displayed starting with Name.

<table id="table_bb4_z34_b2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the event profile. You might select names that describe the following Event Types that are supported and included with the application:-   Clicks Blocked
-   Clicks Permitted
-   Messages Blocked
-   Messages Delivered


</td></tr><tr><td>

Source

</td><td>

Select the source you configured for the integration on the Integration Configurations page.

</td></tr><tr><td>

Order

</td><td>

Order this profile is run. Default is 100.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the profile.

</td></tr><tr><td>

Description

</td><td>

Text to help you identify this event profile.

</td></tr></tbody>
</table>4.  Select **Continue**.

    The Proofpoint Event Selection step is displayed and the supported Event Types included with the application are displayed in the `Available` column:

    -   Clicks Blocked
    -   Clicks Permitted
    -   Messages Blocked
    -   Messages Delivered
5.  Choose one or more to move to the `Selected` column.

6.  Select **Continue**.

    The profile\(s\) you selected are displayed. For example, if you select a messages event, the Message Mapping configuration step is displayed in the progress bar. If you select a message profile and a clicks profile, both configuration steps are displayed in the progress bar.

    The values for the Source Fields are provided on this page from the targeted attack protection \(TAP\) data in your environment as a reference.

    The default mapping of the source fields data to the target fields is displayed on the right side of the page. Basic data is included as a guide, but you can modify this mapping.

7.  Select the **f\(x\)** icon to view the default translations included with the application.

    These translations accommodate multiple values for a field by inserting commas between the values.

8.  Select **Continue**.

9.  In the Filtering and Aggregations page, configure the following:

    |Option|Description|
    |------|-----------|
    |Filter based on conditions for Message Events|Select to enable filtering based on message events.|
    |Message Events Filter Conditions|Create the message event filter conditions.|
    |Filter based on conditions for Click Events|Select to enable filtering based on click events.|
    |Click Events Filter Conditions|Create the click event filter conditions.|
    |Aggregation Conditions|Select to allow an incoming incident to be appended to an open security incident instead of creating a new one.|
    |Incident fields with matching values|Add Security Incident Response fields. All field values that are selected must be matched for an incident to meet an aggregation criteria.|
    |Log work note for New Incident|Select to enable work notes logging to the parent Security Incident Response.|
    |Enable ThreatID Relation|Select to enable aggregation of all the incidents for which the ThreatID is same.|

10. Select **Continue**.

    The Scheduling step is displayed.

11. Select one for the import type and how often you want to import event data.

<table id="choicetable_ehs_bq4_b2c"><thead><tr><th align="left" id="d123864e400">

Option

</th><th align="left" id="d123864e403">

Description

</th></tr></thead><tbody><tr><td id="d123864e409">

**Ongoing Events Ingestion**

</td><td>

Select this to import events on a regular interval. Provide a start date, the end date, and the polling interval in minutes.-   **Polling increment \(minutes\)**: Interval in minutes between imports
-   **Set Initial Events Ingestion Time**
-   **Input initial Ingestion Time**


</td></tr><tr><td id="d123864e433">

**One Time Retrieval**

</td><td>

Select this to import events only once on the basis of the date configured. All the events from the selected date are imported.Provide a start date for the event import \(**Since date**\).

</td></tr></tbody>
</table>12. Select **Finish**.

    Lists the newly created event profile with the existing profiles.


