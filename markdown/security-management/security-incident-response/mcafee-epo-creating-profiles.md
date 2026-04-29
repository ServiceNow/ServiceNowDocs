---
title: McAfee ePO integration capability profiles
description: As a user with the security incident administrator \(sn\_si.admin\) role, you create profiles for the McAfee ePO capabilities in your ServiceNow AI Platform instance. You group queries or actions in profiles and determine which McAfee ePO capabilities you want to run when a new security incident is created.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# McAfee ePO integration capability profiles

As a user with the security incident administrator \(sn\_si.admin\) role, you create profiles for the McAfee ePO capabilities in your ServiceNow AI Platform® instance. You group queries or actions in profiles and determine which McAfee ePO capabilities you want to run when a new security incident is created.

## Capability profiles

You create profiles™ so you can group McAfee ePO capabilities and configure the settings for these capabilities from your ServiceNow AI Platform® instance. You have the flexibility to create multiple profiles for these capabilities, which allows you to determine which actions or queries are invoked when a Security Incident Response \(SIR\) incident is created. To fit the needs of your organization, you can create a single profile that runs queries for system details, initiates malware scans, and isolates host machines, for example, or, you can create multiple profiles, each with its own, single McAfee ePO capability.

<table id="table_cg1_54q_sgb"><thead><tr><th>

Primary purpose of your profile

</th><th>

Set up requirements

</th><th>

McAfee ePO capabilities required for this profile type

</th></tr></thead><tbody><tr><td>

Gather system details

</td><td>

None

</td><td>

**Get Host Details**

</td></tr><tr><td>

Isolate a host

</td><td>

Verify with your McAfee ePO administrator that you have created the security tags for the isolate host action in your McAfee ePO console. For more information, see [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](../task/mcafee-epo-setup-mcafee.md).

</td><td>

**Isolate Host**

</td></tr><tr><td>

Scan and search for threats on your host

</td><td>

Verify with your McAfee ePO administrator that you have created the security tags for the initiate malware scan action in your McAfee ePO console. For more information, see [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](../task/mcafee-epo-setup-mcafee.md).

</td><td>

**Initiate Malware Scan****Note:** As part of the McAfee ePO malware scan, the List Threat Events capability is invoked automatically. However, you are not required to add the List Threat Events capability to the profile with the malware scan capability. Results of the malware scan are displayed on the Threat Event Details tab on the security incident.

</td></tr><tr><td>

Remove isolation for a host

</td><td>

Verify with your McAfee ePO administrator that you have created the security tags for the isolate host action in your McAfee ePO console. For more information, see [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](../task/mcafee-epo-setup-mcafee.md).

</td><td>

**Remove Isolation**

</td></tr><tr><td>

Gather threat enrichment data.

</td><td>

None

</td><td>

**List Threat Events**

</td></tr></tbody>
</table>-   **[Create a capability profile](../task/mcafee-epo-create-profile.md)**  
Create a profile and select the McAfee ePO capabilities that you want the profile to run.
-   **[Defining triggering conditions with a Configuration item \(CI\) field](mcafee-epo-alternate-ci.md)**  
After you create a profile and select the McAfee ePO capabilities that you want the profile to run, you configure the settings of the profile so that it runs only when a set of specific conditions are met.
-   **[Configure settings](mcafee-epo-configuring-profile.md)**  
After you create a profile and select the McAfee ePO capabilities that you want the profile to run, configure the settings so that the profile is invoked only under the specific conditions that you define.

**Parent Topic:**[McAfee ePO integration](mcaffee-epo-overview-arch.md)

**Previous topic:**[Create an approval group](../task/create-approval-group-mcafee.md)

**Next topic:**[Create a capability profile](../task/mcafee-epo-create-profile.md)

