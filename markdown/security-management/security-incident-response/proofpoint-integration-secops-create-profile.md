---
title: Create an event profile for the Proofpoint Integration for Security Operations
description: Create an event profile to identify the events you want to import from the Proofpoint product.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Proofpoint Integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an event profile for the Proofpoint Integration for Security Operations

Create an event profile to identify the events you want to import from the Proofpoint product.

## About this task

You create an event profile by configuring event types, mappings and import schedules. A progress bar on the page displays all the steps and is highlighted for the currently active configuration.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  Navigate to **All** &gt; **SIR Integration with Proofpoint** &gt; **Proofpoint Events Profile**.

2.  On the Events Profiles page, select **New**.

3.  On the form, fill in the fields.

    The progress bar is displayed starting with Name.

<table id="table_bb4_z34_b2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the event profile. Consider using a name that includes the associated event type:-   Clicks Blocked
-   Clicks Permitted
-   Messages Blocked
-   Messages Delivered


</td></tr><tr><td>

Source

</td><td>

The source configured for the integration on the Integration Configurations page.

</td></tr><tr><td>

Order

</td><td>

The order in which this profile is run. The default value is 100.

</td></tr><tr><td>

Active

</td><td>

Option for activating the profile.

</td></tr><tr><td>

Description

</td><td>

Optional description for this event profile.

</td></tr></tbody>
</table>4.  Select **Continue**.

5.  Choose one or more event types by moving them from the **Available** column to the **Selected** column.

    The available event types are:

    -   Clicks Blocked
    -   Clicks Permitted
    -   Messages Blocked
    -   Messages Delivered
6.  Select **Continue**.

    The configuration steps related to the selected event type or types are displayed in the progress bar.

    The values for the Source Fields are provided from the targeted attack protection \(TAP\) data in your environment as a reference.

    The default mapping of the source fields data to the target fields is displayed on the page. Basic data is included as a guide, but you can modify this mapping.

7.  Select the **f\(x\)** icon to view the default translations included with the application.

    Multiple values for a field are separated by commas.

8.  Select **Continue**.

9.  In the Filtering and Aggregations page, configure the properties in the following table.

    |Option|Description|
    |------|-----------|
    |Filter based on conditions for Message Events|Option to enable filtering based on message events.|
    |Message Events Filter Conditions|Message event filter conditions.|
    |Filter based on conditions for Click Events|Option to enable filtering based on click events.|
    |Click Events Filter Conditions|Click event filter conditions.|
    |Aggregation Conditions|Option to allow an incoming incident to be appended to an open security incident instead of creating a new one.|
    |Incident fields with matching values|Add the Security Incident Response fields whose values must be matched for an incident to be included in an aggregation.|
    |Log work note for New Incident|Option to enable work notes to be logged to the parent Security Incident Response.|
    |Enable ThreatID Relation|Option to enable aggregation of all incidents that have matching ThreatIDs.|

10. Select **Continue**.

11. Select one of the import type and how often you want to import event data.

<table id="choicetable_ehs_bq4_b2c"><thead><tr><th align="left" id="d127836e419">

Option

</th><th align="left" id="d127836e422">

Description

</th></tr></thead><tbody><tr><td id="d127836e428">

**Ongoing Events Ingestion**

</td><td>

Option to import events at a regular interval that is defined with a start date, an end date, and the polling interval in minutes.-   **Polling increment \(minutes\)**: Interval in minutes between imports
-   **Set Initial Events Ingestion Time**
-   **Input initial Ingestion Time**


</td></tr><tr><td id="d127836e452">

**One Time Retrieval**

</td><td>

Option to import events only once on the basis of the date configured. All the events from the selected date are imported.Provide a start date for the event import \(**Since date**\).

</td></tr></tbody>
</table>12. Select **Finish**.


## Result

The newly created event profile is included in the list of existing event profiles on the Events Profiles page.

