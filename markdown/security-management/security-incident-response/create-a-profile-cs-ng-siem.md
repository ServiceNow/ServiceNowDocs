---
title: Create a detection profile
description: Determine the CrowdStrike Next-Gen SIEM detections that are suitable for creating security incidents by creating a detection profile in your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Next-Gen SIEM integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a detection profile

Determine the CrowdStrike Next-Gen SIEM detections that are suitable for creating security incidents by creating a detection profile in your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Important:** If no correlation rules are configured in the CrowdStrike portal, the detection profile may display a generic "**No active correlation rules found. Please ensure that correlation rules are configured, activated, and published in your Crowdstrike environment**" message in ServiceNow® instance. To avoid this issue, confirm that at least one correlation rule is created in the CrowdStrike portal before configuring the ingestion profile.

## Procedure

1.  Navigate to **All** &gt; **CrowdStrike Next-Gen SIEM** &gt; **Detection Profile**.

2.  Select **New**.

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

Option for making the profile active.

 When a profile is active, the ServiceNow AI Platform actively polls CrowdStrike Next-Gen SIEM detections and corresponding security detections are created in Security Incident Response when the filtering conditions are matched.

</td></tr><tr><td>

Source

</td><td>

CrowdStrike tenant that you configured to ingest detections. If you have multiple tenants configured, select the appropriate tenant for the detection types you are planning to ingest for the profile.

</td></tr><tr><td>

Order

</td><td>

Priority in which the profiles are executed when two or more profiles share triggering conditions. Priority values are usually provided as 100 \(the default value\), 200, 300, and so on.The profile with the lowest number has the highest priority.

</td></tr><tr><td>

Description

</td><td>

Optional description of the profile.

</td></tr></tbody>
</table>4.  Select **Update** .

    The initial detection profile is created with basic information. Saving the profile at this point enables you to continue with defining the profile in case you are interrupted.

5.  Continue with the profile definition process immediately.

    1.  On the CrowdStrike-Nextgen Detection Profiles page, select the profile you just created.

    2.  In the progress bar, select **Correlation Rules**.


## What to do next

[Set correlation rules](select-correlation-rules-cs-ng-siem.md)

