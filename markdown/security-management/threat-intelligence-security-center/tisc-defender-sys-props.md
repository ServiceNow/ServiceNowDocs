---
title: System properties for Microsoft Defender EDR
description: The following details the system properties for Microsoft Defender EDR.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-04-18"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for EDR Integration, TISC Security Tools integrations, TISC Integrations, Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# System properties for Microsoft Defender EDR

The following details the system properties for Microsoft Defender EDR.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **All** &gt; **Glide properties catalog** &gt; **Glide properties**.

2.  Search for Microsoft Defender properties.

<table id="table_rt2_g5s_1fc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_tisc\_defender.rate\_limiter.minute

</td><td>

This allows the users to limit the rate of sending EDR to MS Defender on minutely basis.-   Type: Integer
-   Value: 100


</td></tr><tr><td>

sn\_tisc\_defender.rate\_limiter.hour

</td><td>

This allows users to limit the rate of sending EDR to MS Defender on an hourly basis.-   Type: Integer
-   Value: 1500


</td></tr></tbody>
</table>
**Parent Topic:**[Microsoft Defender for EDR Integration](../concept/tisc-ms-defender-integration.md)

