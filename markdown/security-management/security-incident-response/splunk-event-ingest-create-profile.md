---
title: Create and name an event profile
description: Create an event profile in your ServiceNow AI Platform instance and determine which Splunk alerts create security incidents.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create and name an event profile

Create an event profile in your ServiceNow AI Platform instance and determine which Splunk alerts create security incidents.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Before ServiceNow AI Platform Security Incident Response \(SIR\) security incidents are created from ingested alerts, the field values from alerts are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be displayed.

From an integration perspective using available APIs, Splunk events are forwarded individually and manually as discreet events, or they are combined into triggered alerts that are automatically ingested into the Security Operations environment of your ServiceNow AI Platform instance. The integration workflows ingest different types of alerts such as unauthorized access attempts and malware, for example.

These alerts are ingested based on the profiles that you configure in the Security Operations environment of your instance. All alerts are initially ingested for a configured alert type in a profile. Ingested alerts can then be further filtered to specify which alerts create security incidents. For example, you may prefer filters that create security incidents only for alerts that are identified as high-risk. Before a profile is activated, and it creates security incidents from ingested alerts, individual field values on the filtered alerts are mapped to corresponding fields on a layout of security incident for a preview.

Alert names for event profiles in your ServiceNow AI Platform instance must be unique and can only be mapped to one active event profile at any given time. These are the triggered alert names that you configured in your Splunk service as part of the setup for the integration. For more information about configuring alerts in your Splunk Enterprise environment, see [Save searches in your Splunk Enterprise console for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest_save_search.md).

The ServiceNow AI Platform ingests specific alerts using the workflows of the integration. All alerts that meet the selection criteria in your Splunk enterprise console are initially ingested into your ServiceNow AI Platform instance.

A profile in your ServiceNow AI Platform is an encapsulation of a Splunk alert in your Splunk enterprise console. There is a one-to-one relationship between alerts that are ingested with a profile and connections to your Splunk enterprise console: one alert for one connection. There is a single https connection to a search head in your Splunk Enterprise console. Multiple alerts can come from a single search head. If you connect to multiple search heads in your Splunk Enterprise console, you must create multiple profiles in your ServiceNow AI Platform instance to ingest these alerts.

Steps to create profiles for scheduled alert ingestion

## Procedure

1.  To create an event profile for an alert, in your ServiceNow AI Platform instance, navigate to **Splunk ES Integration** &gt; **Splunk ES Event Profiles**.

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

Unique name for the profile. If names are not unique, duplicate profile names are not saved. Profile names in your ServiceNow AI Platform instance must be unique.

</td></tr><tr><td>

Active

</td><td>

Check box is cleared by default. The Active option is disabled and not available for selection till you complete all the profile configuration steps and click **Finish**.

</td></tr><tr><td>

Type

</td><td>

Select the profile type from the choice list. -   Scheduled Alert Ingestion - This type of profile supports triggered alerts that are ingested on a schedule that you configure. Fill in the fields and click **Continue** to proceed to the Alert Selection step of the profile.
-   Manual Event Forwarding - This type of profile supports individual events that are forwarded manually from your Splunk Enterprise console on demand. See the following steps to fill out the form for these types of profiles.


</td></tr><tr><td>

Source Type

</td><td>

Splunk server or search end that you configured to ingest alerts. If you have multiple Splunk servers configured, select the appropriate server for the alert types that your are planning to ingest for the profile. You are required to enter a value.

</td></tr><tr><td>

Order

</td><td>

Default is 100. Leave this setting at the default.If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share the same triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>    The following figure is an example of a completed form for a scheduled alert.

    ![Completed profile name form for a scheduled alert.](../image/Splunk_215_ProfileNameTab.png)

5.  For a profile with a scheduled alert, choose one option to continue with the profile configuration.

    |Option|Description|
    |------|-----------|
    |**Continue**|Save the profile and progress to the Alert Selection step.|
    |**Update**|Save updates to this profile and return to the Splunk Event Profiles list.|
    |**Save**|Save this profile and remain on the page.|
    |**Delete**|Delete this profile record and return to the Splunk Event Profiles list.|

    Steps to create profiles for manual event forwarding

6.  To create a profile that supports manual event forwarding, follow these steps.

    For events that you forward on-demand from your Splunk enterprise console, you can base the individual field mapping on any existing profile. Alternatively, you can create a new mapping grid for exported attachment data. Events that you forward manually are not scheduled in the event profile.

    1.  If not already selected, in the choice list for the Type field, select **Manual Event Forwarding**.

    2.  In the Mapping Option field that is displayed, from the choice list, choose one mapping option to continue.

        Refer to the following figures and tables for more information about the available mapping options in the Mapping Options choice list.

        ![Mapping Option field highlighted.](../image/splunk-manualevent1.png "Create a new field mapping option")

<table id="table_psp_nxq_chb"><thead><tr><th>

Option or field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create new field mapping option

</td><td>

New field mapping for your event. If you do not have an existing field mapping that is similar to the profile that you are creating, select this option to create a new map.

</td></tr><tr><td>

Default profile

</td><td>

Default event forwarding profile for all Splunk events. Default is cleared \(disabled\).

 When this option is enabled, this profile becomes the default profile for manual event forwarding. This profile is the only profile that is active and used for every Splunk event field mapping to a SIR security incident. One profile fits all forwarded events.

 The Source field is unavailable if the default profile option is enabled.

</td></tr><tr><td>

Source type

</td><td>

Splunk server.

 This field is unavailable if the default profile option is enabled.

 If available, the Source Type option permits unique event field mapping to security incident fields based on the Splunk source type.

 If you want to manage firewall log events differently than endpoint detection events, and they have different Splunk source types, you can create different event profiles based on source types to accomplish this requirement.

</td></tr><tr><td>

Order

</td><td>

Default is 100. Leave this setting at the default.If you have created a large number of profiles, this value provides a run time execution priority when two or more profiles share triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>        For a profile with a new field mapping, verify that you have entered a value in the Source type field and click **Continue** to proceed to the mapping step of the configuration.

        For a profile with an existing field mapping, refer to the following figure and table for more information.

        ![Copy an existing mapping option.](../image/copy_mapping.png "Select existing profile for field mapping option")

<table id="table_epm_wqf_dhb"><thead><tr><th>

Option or field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select existing profile for field mapping

</td><td>

An existing field mapping for your event. The Copy from profile field is displayed.

 Follow these steps to copy an existing field mapping for this profile.

 1.  To the left of the Copy from profile field that is displayed, click the search icon.
2.  In the Splunk Event Profiles list that is displayed, click the profile name that has the map that you want to copy.

The profile name is displayed in the Copy from profile field.

</td></tr><tr><td>

Default profile

</td><td>

Default event forwarding profile for all Splunk events. Default is cleared \(disabled\).

 When this option is enabled, this profile becomes the default profile for manual event forwarding. This profile is the only profile that is active. It is used for every Splunk event field mapping to a SIR security incident. One profile fits all forwarded events.

 The Source field is unavailable if the default profile option is enabled.

</td></tr><tr><td>

Source type

</td><td>

Splunk server.

 This field is unavailable if the default profile option is selected.

 If available, the Source Type option permits unique event field mapping to security incident fields based on the Splunk source type.

 If you want to manage firewall log events differently than endpoint detection events, and they have different Splunk source types, you can create different event profiles based on source types to accomplish this requirement.

</td></tr><tr><td>

Order

</td><td>

Default is 100. Leave this setting at the default.If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>        At the bottom of the form for selecting an existing mapping for your profile, click **Finish** to complete the profile configuration.


## What to do next

You have successfully completed the steps to create profiles for both scheduled alerts and manual event forwarding. For profiles for manual event forwarding, you have completed the profile configuration. The next step is to load attachment data in the mapping step.

For profiles for scheduled alerts, the next step is to select alerts for automatic ingestion.

-   **[Select scheduled alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-alert-selection.md)**  
After you have created a profile for a scheduled alert, select a Splunk alert for this profile that you want to map to a ServiceNow AI Platform Security Incident Response security incident.
-   **[Mapping alerts and events for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-mapping.md)**  
After you identify the sources for scheduled alert ingestion or manual event forwarding, the next step is to map individual event fields to the fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
-   **[Map alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-map-alerts.md)**  
During the event field-mapping step, you map individual event fields from triggered alerts or imported event data to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
-   **[Preview security incident for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-preview.md)**  
After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform® Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the alert fields that you want displayed on the security incident.
-   **[Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-schedule.md)**  
For automated alert ingestion profiles, this step is final step of the event profile configuration. During this step, you can verify the default settings for alert retrieval or modify the scheduling as needed. This step permits you to filter your alert retrieval based on a date range.

**Parent Topic:**[Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow](../concept/splunk-event-ingest-overview.md)

**Previous topic:**[Configure Splunk Enterprise Event Ingestion settings](configure-splunk-enterprise-event-ingestion-settings.md)

**Next topic:**[Select scheduled alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-alert-selection.md)

