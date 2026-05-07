---
title: Create a capability profile
description: Create a profile and select the McAfee ePO capabilities that you want the profile to run.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Capability profiles, McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a capability profile

Create a profile and select the McAfee ePO capabilities that you want the profile to run.

## Before you begin

Role required: ServiceNow AI Platform® Security incident administrator \(sn\_si.admin\)

## About this task

For this step of the configuration, you create a profile for the McAfee ePO capabilities. When you create profiles, consider the intention of the profile before you add McAfee ePO capabilities to it. Refer to the following table when you create profiles.

The following table lists the capabilities that you are required to add to a profile if you want the profile perform certain queries or actions. Create a single profile that runs queries for host details, initiates malware scans, remove isolation, and isolates host machines, or, create multiple profiles, each with its own, single capability.

## Procedure

1.  Navigate to **McAfee ePO Integration** &gt; **McAfee ePO Capability Profiles**.

    The McAfee ePO Capability Profiles list is displayed.

2.  Click **New**.

3.  On the form, fill the fields.

<table id="choicetable_kn1_ffj_fyb"><thead><tr><th align="left" id="d159985e106">

Field

</th><th align="left" id="d159985e109">

Description

</th></tr></thead><tbody><tr><td id="d159985e115">

**Name**

</td><td>

Name for the McAfee ePO capability profile. This name helps you identify the profile type and describe it. An example for a profile that runs queries is, Host and Threat Details. This name is also the name for the security tag for this profile by default.

</td></tr><tr><td id="d159985e127">

**Description**

</td><td>

Additional information about the profile that further describes the activities of the profile. An example description for a profile that runs queries is, Threat enrichment for system details and a list of threat events. An example description for a profile that runs actions is, Isolate host machine.

</td></tr><tr><td id="d159985e136">

**Source**

</td><td>

Name of the McAfee ePO server. Only configured servers are available from the choice list.

</td></tr><tr><td id="d159985e148">

**McAfee ePO Capability**

</td><td>

Capabilities of the McAfee ePO profile. McAfee ePO supports the following capabilities:-   Get Host Details
-   Isolate Host Profile
-   Initiate Malware Scan
-   Remove Isolation
-   List Threat Events
Select the capabilities you want for this profile from the **Available** column and move them to the **Selected** column.

You can't add Get Host Details, Initiate Malware Scan and List Threat Events in the same profile, and you can't add Remove Isolation and Isolate Host on the same profile.

</td></tr><tr><td id="d159985e188">

**Order**

</td><td>

Workflow priority. Default is 100. The value of this field indicates the order that workflows are executed when two or more profiles share triggering conditions. The workflow with the lowest number has the highest priority.

To set the order of operation, enter a value. For example, 100, 200, 300, 400.

</td></tr><tr><td id="d159985e200">

**Active**

</td><td>

The check box is selected by default to indicate that the profile is active. When selected, the profile is active and triggers automatically when a security incident is created that matches the filtering conditions that you specify during the configuration step.

 When inactive, the profile will not run, and it is not available to invoke from a list.

</td></tr></tbody>
</table>    ![McAfee EPO capability profile details](../image/mcafee-epo-profile-name.png)

4.  To save and validate the profile, click **Continue**.

    If validation is successful, the page reloads and the **Configuration** form is displayed.


## What to do next

The next step is to configure your profile. Before you configure the settings for the profile, you may prefer to review the concepts for configuring profiles and triggering conditions. See [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](mcafee-epo-setup-mcafee.md) and [Defining triggering conditions with a Configuration item \(CI\) field](../concept/mcafee-epo-alternate-ci.md) for more information.

**Parent Topic:**[McAfee ePO integration capability profiles](../concept/mcafee-epo-creating-profiles.md)

