---
title: Rate limit configuration in Microsoft Defender for Endpoint integration
description: Configure the rate limit of the API and timeout for the rate limit for Microsoft Defender for Endpoint integration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Rate limit configuration in Microsoft Defender for Endpoint integration

Configure the rate limit of the API and timeout for the rate limit for Microsoft Defender for Endpoint integration.

## Before you begin

Role required: sn\_si.admin, sn\_si.analyst \(read-only\)

## Procedure

1.  In the navigation filter, enter `sys.properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Search and modify the following properties as per your requirements.

<table id="table_jcd_qkf_fxb"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sec\_defender\_ep.rate\_limit\_timeout\_in\_minutes

</td><td>

If a request does not execute within the specified time frame, the execution gets halted and an appropriate error message is displayed.Default value: 75.

</td></tr><tr><td>

sn\_sec\_defender\_ep.request\_per\_hour\_limit

</td><td>

If the configured API call is made on the same Endpoint within one hour, the request gets queued until the threshold is reached or the configured timeout.Default value: 1500.

</td></tr><tr><td>

sn\_sec\_defender\_ep.request\_per\_minute\_limit

</td><td>

If the configured API call is made on the same Endpoint within one minute, the request gets queued until the threshold is reached or the configured timeout.Default value: 100.

</td></tr><tr><td>

sn\_sec\_defender\_ep.import\_indicator\_request\_per\_minute\_limit

</td><td>

If the configured API call is made on the endpoint within one minute, the request gets queued until the threshold is reached or the configured timeout.Default value: 30.

</td></tr></tbody>
</table>
