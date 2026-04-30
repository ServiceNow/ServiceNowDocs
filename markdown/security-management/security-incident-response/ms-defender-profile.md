---
title: Create an incident profile
description: Determine the Microsoft Defender incidents that are suitable for creating security incidents by creating an incident profile in your ServiceNow AI Platform instance.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-01-05"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an incident profile

Determine the Microsoft Defender incidents that are suitable for creating security incidents by creating an incident profile in your ServiceNow AI Platform® instance.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  Navigate to **All** &gt; **Microsoft Defender Integration** &gt; **Defender Incident Profiles**.

2.  Select **New** to create a new profile.

3.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the profile.

 This name is also the default name for the security tag associated with this profile.

</td></tr><tr><td>

Active

</td><td>

Option to make the profile active.

 When a profile is active, the ServiceNow AI Platform® actively polls incidents and corresponding security incidents are created in Microsoft ServiceNow AI Platform® when the filtering conditions are matched.

</td></tr><tr><td>

Source

</td><td>

Microsoft tenant that you configured to ingest incidents. If you have multiple tenants configured, select the appropriate tenant for the incident types you are planning to ingest for the profile.

</td></tr><tr><td>

Order

</td><td>

Priority in which the profiles are executed when two or more profiles share triggering conditions. Priority values are provided as 100 \(the default value\), 200, 300, and so on.The profile with the lowest number has the highest priority.

</td></tr><tr><td>

Description

</td><td>

Optional description of the profile.

</td></tr></tbody>
</table>    ![Create an incident profile](../image/ms-def-name.png)

4.  Select **Continue**.

    The initial incident profile is created with basic information. Saving the profile at this point enables you to continue with defining the profile in case you’re interrupted.

5.  Continue with the profile definition process immediately.

    1.  Select the profile you created.

    2.  Select **Mapping** in the progress bar.


## What to do next

[Map incident fields](microsoft-defender-mapping.md)

