---
title: Create a capability profile for the CrowdStrike Falcon Insight integration
description: Create a profile and select the CrowdStrike Falcon Insight capabilities that you want the profile to run.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a capability profile for the CrowdStrike Falcon Insight integration

Create a profile and select the CrowdStrike Falcon Insight capabilities that you want the profile to run.

## Before you begin

Role required: sn\_si.admin

## About this task

Consider why you want to create a profile before you add CrowdStrike Falcon Insight capabilities to it. The following table lists the capabilities that you must add to a profile when you want the profile to perform certain queries or actions.

You can create a single profile that runs queries for system details, lists logged-in users, fetches running services, fetches running processes, fetches network statistics, isolates the host, and removes the isolated host. Alternatively, you can create multiple profiles, each with its own single capability.

**Note:** Isolate host, remove isolation, and get file capabilities can’t be merged with any other capabilities while creating a profile.

<table id="table_sqk_k1h_p4b"><thead><tr><th>

Profile purpose

</th><th>

CrowdStrike capabilities

</th></tr></thead><tbody><tr><td>

Gather host details and logged-in users

</td><td>

-   **Get Host Details**
-   **Get Logged On Users**

</td></tr><tr><td>

Fetch the network statistics, processes, and services running for a host

</td><td>

-   **Get Network Statistics**
-   **Get Running Processes**
-   **Get Running Services**

</td></tr><tr><td>

Isolate a host

</td><td>

**Isolate Host**

</td></tr><tr><td>

Remove isolation for a host

</td><td>

**Remove Isolation**

</td></tr><tr><td>

Obtain a file from a host endpoint

</td><td>

**Get File**

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **CrowdStrike Falcon Insight Integration** &gt; **CrowdStrike Capability Profiles**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_r1k_4ch_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the new capability profile. This name helps you to identify the profile type and is also the default name for the security tag that is associated with this profile.

</td></tr><tr><td>

Active

</td><td>

Indicates if the profile is active or not.When the profile is active, it automatically triggers when a security incident is created that matches the filtering conditions that you’ve specified in the configuration.

</td></tr><tr><td>

Description

</td><td>

Unique description for the capability profile.

</td></tr><tr><td>

Source

</td><td>

Name of the server. You can only view previously configured servers from the list.

</td></tr><tr><td>

Order

</td><td>

Flow priority. The value for this field indicates the order that flows are executed when two or more profiles share triggering conditions.

 The flow with the lowest number has the highest priority. To set the order of operation, enter a value. For example, 100, 200, 300, 400.

 Default: 100

</td></tr><tr><td>

CrowdStrike Falcon Insight Capabilities

</td><td>

Capabilities of the CrowdStrike Falcon Insight profile.Select the capabilities that you want for this profile from the **Available** to the **Selected**column.

</td></tr></tbody>
</table>    The following example shows a complete form for a profile with the Get System Details capability.

    ![Falcon Insight Profile Details.](../image/falcon-insight-profile-details.png)

4.  Click **Next**.


## What to do next

Now you can[configure your profile](configure-profiles-and-security-incidents-for-the-crowdstrike-falcon-insight-integration.md). Ensure that you have [reviewed the concepts for configuring profiles and trigger conditions](../concept/define-trigger-conditions.md) before you configure the profile.

