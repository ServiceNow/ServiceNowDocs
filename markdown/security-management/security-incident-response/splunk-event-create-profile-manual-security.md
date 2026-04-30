---
title: Create a profile
description: You can set up a profile for manual forwarded events.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Set up a profile for manual event forwarding, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a profile

You can set up a profile for manual forwarded events.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  To create a profile that supports manual event forwarding, follow these steps.

    For events that you forward on-demand from your Splunk Enterprise Security console, you can base the individual field mapping on any existing profile. Alternatively, you can create a new mapping grid for exported attachment data. Events that you forward manually are not scheduled in the event profile.

    1.  If not already selected, in the choice list for the Type field, select **Manual Event Forwarding**.

    2.  In the Mapping Option field that is displayed, from the choice list, choose one mapping option to continue.

        Refer to the following figures and tables for more information about the available mapping options in the Mapping Options choice list.

        ![Splunk: manual event forwarding](../image/splunk-manualevent1-security.png)

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

Default event forwarding profile for all Splunk events. Default is cleared \(deactivated\).

 When this option is enabled, this profile becomes the default profile for manual event forwarding. This profile is used when there is no match on source from the manually forwarded event. It becomes the default profile for all events with unknown sources.

 The Source field is unavailable if the default profile option is enabled.

</td></tr><tr><td>

Source \(Notable Event field\)

</td><td>

This is a field that typically defines the correlation rule that triggered the notable, for example, Brute Force Attacks. This field is unavailable if the default profile option is enabled.

 If available, this field permits unique event field mapping to security incident fields based on the splunk correlation rule that is typically different for different event types.

 If you want to manage different correlation rules separately, you can create different profile event profiles based on correlation rule to accomplish this requirement.

</td></tr><tr><td>

Automate Notable Event Updates

</td><td>

Select this check box if you want to update the notable event status and add additional comments when a SIR incident is created from the notable event and / or when the SIR incident is closed. This will occur for both the initial triggering notable events that creates the SIR incident, as well as aggregated events.

</td></tr><tr><td>

Source \(Splunk Server\)

</td><td>

The Splunk server that you configured as the source for notable events. If you have multiple Splunk servers configured, select the appropriate server for the notable event types that will be updated for the profile. You are required to enter a value.

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

        ![Manual: existing profile](../image/copy_mapping_security.png)

<table id="table_epm_wqf_dhb"><thead><tr><th>

Option or field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select existing profile for field mapping

</td><td>

Reuse an existing field mapping for your new notable event profile. The Copy from profile field is displayed. Follow these steps to copy an existing field mapping for this profile.

 1.  To the left of the Copy from profile field that is displayed, click the search icon.
2.  In the Splunk ES Event Profiles list that is displayed, click the profile name that has the map that you want to copy.

The profile name is displayed in the Copy from profile field.

</td></tr><tr><td>

Default profile

</td><td>

Default event forwarding profile for all Splunk notable events with unmatched source. Default is cleared \(disabled\).

 When this option is enabled, this profile becomes the default profile for manual event forwarding.

 The Source field is unavailable if the default profile option is enabled.

</td></tr><tr><td>

Source \(Notable Event field\)

</td><td>

This is a field that typically defines the correlation rule that triggered the notable, for example, Brute Force Attacks. This field is unavailable if the default profile option is enabled.

 If available, this field permits unique event field mapping to security incident fields based on the splunk correlation rule that is typically different for different event types.

 If you want to manage different correlation rules separately, you can create different profile event profiles based on correlation rule to accomplish this requirement.

</td></tr><tr><td>

Automate Notable Events

</td><td>

Select this check box if you want to update the notable event status and add additional comments when a security incident is created from the notable event or when the security incident is closed. This occurs for both the initial triggering notable events that creates the security incident, as well as aggregated events.

</td></tr><tr><td>

Source \(Splunk Server\)

</td><td>

Splunk server or search end that you configured as the source for notable events. If you have multiple Splunk servers configured, select the appropriate server for the notable event types that will be updated for the profile. You are required to enter a value.

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


