---
title: Create a capability profile for the Microsoft Defender for Endpoint integration
description: Create a profile and select the Microsoft Defender for Endpoint capabilities that you want the profile to run.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a capability profile for the Microsoft Defender for Endpoint integration

Create a profile and select the Microsoft Defender for Endpoint capabilities that you want the profile to run.

## Before you begin

Role required: sn\_si.admin

## About this task

Profiles are created to club or group the capabilities together, which would help Analysts perform the investigation or remediation easily. You can add the following capabilities to the profile:

-   Get Host Details
-   Get Logged On Users
-   Isolate Host
-   Remove Isolation

You cannot club Isolate Host and Remove Host Isolation capabilities with other capabilities while creating a profile. Profiles for these capabilities have to be individually created. While on the other hand, the Get Host Details and Get Logged on Users capabilities can be clubbed together. You could create profiles individually or by clubbing them in full or parts as per your requirement.

**Note:** After a capability is included in a profile, it cannot be included in any other profile from the same source.

## Procedure

1.  Navigate to **Microsoft Defender for Endpoint** &gt; **Capability Profiles**.

    The Microsoft Defender for Endpoint capability profiles list is displayed.

    ![Create a new capability profile for the Microsoft Defender for Endpoint integration](../image/capability_profile.png "Profile Configuration")

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_lbw_ycv_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Microsoft Defender for Endpoint capability profile. This name helps you identify the profile type and describe it.

</td></tr><tr><td>

Description

</td><td>

Additional information about the profile that further describes the profile.

</td></tr><tr><td>

Source

</td><td>

Name of the Microsoft Defender for Endpoint source. Only configured sources are available from the list.

</td></tr><tr><td>

Microsoft Defender for Endpoint capabilities

</td><td>

Capabilities of the Microsoft Defender for Endpoint profile. Select the capabilities you want for this profile from the Available column, and move them to the Selected column.

</td></tr><tr><td>

Order

</td><td>

Flow priority. Default is 100. The value of this field indicates the order that flows are executed when two or more profiles share triggering conditions.The flow with the lowest number has the highest priority.

 To set the order of operation, enter a value. For example, 100, 200, 300, 400.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the profile is active. After the profile is active, the profile is automatically triggered when a security incident is created that matches the filtering conditions that you have specified in the configuration.

</td></tr></tbody>
</table>4.  To continue to Profile Configuration, click **Next**.


## What to do next

The next step is to configure your profile. Before you configure the settings for the profile, you may prefer to review the how profiles and configured and triggering conditions. For more information, see [Trigger conditions in a configuration item](../reference/trigger-conditions-configuration-item.md).

