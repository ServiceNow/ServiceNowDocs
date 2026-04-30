---
title: Create an incident profile
description: Determine the Cortex XSIAM incidents that are suitable for creating security incidents by creating an incident profile in your ServiceNow AI Platform instance.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-11-10"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an incident profile

Determine the Cortex XSIAM incidents that are suitable for creating security incidents by creating an incident profile in your ServiceNow AI Platform® instance.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks XSIAM** &gt; **XSIAM Profile**.

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

 When a profile is active, the ServiceNow AI Platform® actively polls XSIAM incidents and corresponding security incidents are created in ServiceNow AI Platform® when the filtering conditions are matched.

</td></tr><tr><td>

Source

</td><td>

XSIAM tenant that you configured to ingest incidents. If you have multiple tenants configured, select the appropriate tenant for the incident types you are planning to ingest for the profile.

</td></tr><tr><td>

Order

</td><td>

Priority in which the profiles are executed when two or more profiles share triggering conditions. Priority values are provided as 100 \(the default value\), 200, 300, and so on.The profile with the lowest number has the highest priority.

</td></tr><tr><td>

Description

</td><td>

Optional description of the profile.

</td></tr></tbody>
</table>    ![Create an incident profile](../image/xsiam-name.png)

4.  Select **Continue**.

    The initial incident profile is created with basic information. Saving the profile at this point enables you to continue with defining the profile in case you’re interrupted.

5.  Continue with the profile definition process immediately.

    1.  Select the profile you created.

    2.  Select **Alert Sources** in the progress bar.


## What to do next

[Set Alert Sources](pan-cortex-xsiam-rules.md)

