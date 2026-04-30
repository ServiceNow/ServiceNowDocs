---
title: Create a detection profile for CrowdStrike Next-Gen SIEM
description: Determine the CrowdStrike Next-Gen SIEM detections that are suitable for creating security incidents by creating a detection profile in your ServiceNow AI Platform instance.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-06-30"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Next-Gen SIEM integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a detection profile for CrowdStrike Next-Gen SIEM

Determine the CrowdStrike Next-Gen SIEM detections that are suitable for creating security incidents by creating a detection profile in your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin because the sn\_si.admin role inherits the required permissions by default.

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

[Set correlation rules for CrowdStrike Next-Gen SIEM integration](select-correlation-rules-cs-ng-siem.md)

