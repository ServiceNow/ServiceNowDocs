---
title: Create CrowdStrike API client and generate keys
description: Create the CrowdStrike API client and generate the client ID and key, which you use to configure the CrowdStrike Falcon Insight integration.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create CrowdStrike API client and generate keys

Create the CrowdStrike API client and generate the client ID and key, which you use to configure the CrowdStrike Falcon Insight integration.

## Before you begin

Role required: CrowdStrike Falcon administrator

## Procedure

1.  On the CrowdStrike Falcon Platform, navigate to **API Clients and Keys**.

2.  In the OAuth2 API Clients table, click **Add new API client**.

3.  Enter the following details to define your API client:

<table id="table_fcy_zdp_fpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Client Name

</td><td>

Enter the client name. This field is required.

</td></tr><tr><td>

Description

</td><td>

Enter the description for the client name.

</td></tr><tr><td>

API Scopes

</td><td>

Defining the scopes is required. **Important:** Ensure that you enable the API account, and make sure that the following scopes are enabled for the API account:

-   Enable Read and Write scopes for Hosts API
-   Enable Read scope for Indicators API


</td></tr></tbody>
</table>4.  Click **Add** to save the API client and generate the client ID and secret key.


