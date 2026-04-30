---
title: Create a profile for Microsoft Azure Sentinel
description: Create an incident profile in your ServiceNow AI Platform instance and determine the Microsoft Azure Sentinel incidents that are suitable for creating security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a profile for Microsoft Azure Sentinel

Create an incident profile in your ServiceNow AI Platform instance and determine the Microsoft Azure Sentinel incidents that are suitable for creating security incidents.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

The integration enables you to create different types of incidents, such as unauthorized access attempts and malware. These incidents are created based on the profiles that you configure in the ServiceNow AI Platform instance. All incidents are initially created for a configured incident type in a profile. Created incidents can then be further filtered to specify which incidents create security incidents.

All incidents that meet the selection criteria in your Microsoft Azure tenant, and are available over the Microsoft Azure Sentinel API, are initially ingested into your ServiceNow AI Platform instance.

## Procedure

1.  Navigate to **All** &gt; **Microsoft Azure Sentinel Integration** &gt; **Azure Sentinel Incident Profile**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the profile.

 This name helps you to identify the profile type and is also the default name for the security tag that is associated with this profile.

</td></tr><tr><td>

Active

</td><td>

Indicator that the profile is active.

 When the profile is active, it implies that the ServiceNow AI Platform is actively polling Azure Sentinel incidents and that corresponding security incidents are created in SIR when the filtering conditions are matched.

</td></tr><tr><td>

Source

</td><td>

Microsoft Azure tenant that you configured to ingest incidents. If you have multiple tenants configured, select the appropriate tenant for the incident types that you are planning to ingest for the profile.

</td></tr><tr><td>

Order

</td><td>

Flow priority. The value for this field indicates the order that flows are executed when two or more profiles share triggering conditions.

 The flow with the lowest number has the highest priority.

To set the order of operation, enter a value. For example, 100, 200, 300, 400.The default is 100.

</td></tr><tr><td>

Description

</td><td>

Extra text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>4.  To move to the Mapping section, click **Continue**.


## What to do next

Map individual Microsoft Azure Sentinel incident fields to the fields on the ServiceNow AI Platform SIR security incident.

