---
title: Create a profile
description: You can set up a profile so that notable events are automatically ingested.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up a profile for scheduled notable event ingestion, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a profile

You can set up a profile so that notable events are automatically ingested.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  To create an event profile for a notable event or correlation rule type in your ServiceNow AI Platform instance, navigate to **Splunk Integration** &gt; **Splunk Event Profile**.

2.  If the Splunk Event Profile form is not displayed, click **Name** in the Progress bar.

3.  Click **New**.

4.  Fill in the fields.

    An example of a completed form follows the table.

<table id="simpletable_kt2_lqb_jfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the profile. If names are not unique, an error will be displayed and duplicate profile names are not saved. Profile names in your ServiceNow AI Platform instance must be unique.

</td></tr><tr><td>

Active

</td><td>

Check box is cleared and disabled by default. You should complete all sections in the profile before making it active.

</td></tr><tr><td>

Type

</td><td>

Select the profile type from the choice list. -   Scheduled Event Ingestion: This type of profile supports notable events that are ingested on a configured schedule. Fill in the fields.
-   Manual Event Forwarding: This type of profile supports notable events that are forwarded manually from your Splunk Enterprise Security Incident Review console on demand. See the following steps to fill out the form for these types of profiles.


</td></tr><tr><td>

Source

</td><td>

Splunk server or search end that you configured to ingest notable events. If you have multiple Splunk servers configured, select the appropriate server for the notable event types that will be ingested for the profile. You are required to enter a value.

</td></tr><tr><td>

Order

</td><td>

Default is 100. If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share the same triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Additional text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>    The following figure is an example of a completed form for a scheduled notable event type.

    ![Splunk ES Event Profile](../image/new-images/notable-event-profile.png)

5.  For a profile with a scheduled notable event, choose one option to continue with the profile configuration.

    |Option|Description|
    |------|-----------|
    |**Continue**|Save the profile and progress to the Event Selection step.|
    |**Update**|Save updates to this profile and return to the Splunk Event Profiles list.|
    |**Save**|Save this profile and remain on the page.|
    |**Delete**|Delete this profile record and return to the Splunk Event Profiles list.|


## What to do next

The next step is to select notable events for automatic ingestion.

