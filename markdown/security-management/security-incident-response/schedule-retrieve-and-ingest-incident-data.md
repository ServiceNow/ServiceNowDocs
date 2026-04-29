---
title: Schedule Microsoft Azure Sentinel incident retrieval
description: Set a schedule to retrieve the incident data and to ingest the Microsoft Azure Sentinel incidents that match the criteria in the profile.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule Microsoft Azure Sentinel incident retrieval

Set a schedule to retrieve the incident data and to ingest the Microsoft Azure Sentinel incidents that match the criteria in the profile.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

You can plan how often you want to poll for future Microsoft Azure Sentinel incidents that match the incident profile configuration.

To enable automated incident ingestion, you must configure the scheduling and incident retrieval before you activate the profile. To define a specific date and time for the initial ingestion, enable **set incident ingestion time**. Subsequent ingestion is based on the polling interval period.

The polling interval is configured for each profile individually. The different polling intervals may impact the performance of the Microsoft Azure Sentinel incident integration. When scheduling, plan to balance the system load against the urgency of an incident. A one-minute default value is set for all profiles. You can modify this setting based on the urgency of the incident and the anticipated load on your system.

Any alerts that gets added to the incident in a particular polling interval there will be a process executed and then appended to the Azure Sentinel alerts related lists and worknote is also posted.

## Procedure

1.  On the scheduling form, fill in the fields.

    Configure the schedule to define how and when you pull incidents from the Microsoft Azure tenant.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ongoing incident ingestion

</td><td>

Ongoing incident ingestion that the ServiceNow AI Platform instance pulls from the Microsoft Azure tenant for new incidents. Security incidents are created if triggered incidents are found and the incident generation filtering criteria matches.

</td></tr><tr><td>

Polling increment \(minutes\)

</td><td>

Polling frequency that is defined in minutes.

</td></tr><tr><td>

Set incident ingestion time

</td><td>

Incident ingestion that is based on the configured date and time.You can use this option to define a specific date and time for the initial ingestion. Subsequent ingestions are based on the polling interval period.

</td></tr><tr><td>

Input incident ingestion time

</td><td>

Date and time that you specify for the incident ingestion.

</td></tr><tr><td>

One-Time Retrieval

</td><td>

Select this checkbox to allow one-time retrieval of historical Azure Sentinel incidents and then do the reconciliation of the data. When you select this checkox, the application will pull all the open and closed Azure Sentinel incidents for the period upto 6 months approximately.When processing the data both ongoing incidents and historical data both are pulled, but the processing of the ongoing incidents takes precedence over historical pull and otherwise the historical pull may take some time based on the duration as well as the number of incidents that you are ingesting.

**Note:** The retrieved historical Azure Sentinel incidents undergo de-duplication checks to prevent any duplicates within the Security Incident Response application.

</td></tr><tr><td>

Since date

</td><td>

The date since when the historical incidents are ingested from Azure Sentinel.**Note:** The incident data is approximately pulled from the past 6months.

</td></tr></tbody>
</table>    The scheduling page enables you to define how and when incidents are pulled from the Microsoft Azure tenant.

2.  To navigate to the Additional Options page, click **Continue**.


