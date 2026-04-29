---
title: Create a capability profile for the FireEye Endpoint integration
description: Create a profile and select the FireEye HX capabilities that you want the profile to run.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a capability profile for the FireEye Endpoint integration

Create a profile and select the FireEye HX capabilities that you want the profile to run.

## Before you begin

Role required: NowPlatform Security incident administrator \(sn\_si.admin\)

## About this task

Profiles are created to club capabilities together, and would help Analysts perform the investigation/remediation easily.

Following are the list of capabilities that you could add to profile\(s\):

1.  Get Host Details
2.  Get Logged On Users
3.  Get Network Statistics
4.  Get Running Processes
5.  Get Running Services
6.  Get File
7.  Isolate Host
8.  Remove Isolation

You cannot club Get File, Isolate Host, and Remove Host Isolation capabilities with other capabilities while creating a profile. Profiles for these have to be individually created. On the other hand, Get System Details, Get Logged on Users, Get Network Stats, Get Running Processes, and Get Running Services can be clubbed together. You could create profiles individually or by clubbing them in full or parts as per your need. Once a capability is included in a profile, it cannot be included in another profile.

To create a new capability profile, follow these steps:

## Procedure

1.  Navigate to **FireEye Integration** &gt; **FireEye Capability Profiles**.

    The capability profiles list is displayed.

2.  Click **New**.

3.  On the form, fill the fields.

<table id="table_igp_yq1_pqb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the FireEye HX capability profile. This name helps you identify the profile type and describe it.

</td></tr><tr><td>

Description

</td><td>

Additional information about the profile that further describes the profile.

</td></tr><tr><td>

Source

</td><td>

Name of the FireEye HX source. Only configured sources are available from the choice list.

</td></tr><tr><td>

FireEye HX Capabilities

</td><td>

Capabilities of the FireEye HX profile. Select the capabilities you want for this profile from the Available column and move them to the Selected column.

</td></tr><tr><td>

Order

</td><td>

Flow priority. Default is 100. The value of this field indicates the order that Flows are executed when two or more profiles share triggering conditions.The Flow with the lowest number has the highest priority.

 To set the order of operation, enter a value. For example, 100, 200, 300, 400.

</td></tr><tr><td>

Active

</td><td>

This indicates that the profile is active. When the profile is active, it automatically triggers when a security incident is created that matches the filtering conditions that you have specified in the configuration.

</td></tr></tbody>
</table>    ![capability profile.](../image/fireeye-profile-config.png)

    The following figure is an example of a completed form for profile details with Get Host Details capability.

4.  Click **Next** to continue to Profile Configuration.

    ![Capability profile](../image/fireeye-profile-config.png)

    **Note:** Isolate Host, Remove Host Isolation and Get File capabilities cannot be clubbed with other capabilities.


## What to do next

The next step is to configure your profile. Before you configure the settings for the profile, you may prefer to review the concepts for configuring profiles and triggering conditions. For more information, see Understand how trigger conditions work with a configuration item for a profile.

