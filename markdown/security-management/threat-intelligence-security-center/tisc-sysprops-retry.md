---
title: System properties for Webhooks
description: The system properties for webhooks are explained below.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Webhooks, Administer, Threat Intelligence Security Center, Security Operations]
---

# System properties for Webhooks

The system properties for webhooks are explained below.

<table id="table_zp1_pbb_2cc"><thead><tr><th>

Property Name

</th><th>

Description

</th><th>

Type

</th><th>

Value

</th></tr></thead><tbody><tr><td>

sn\_sec\_tisc.webhook\_ignore\_threat\_score\_reapply

</td><td>

Ignore webhook events triggered by threat score recalculate history.

</td><td>

True/False

</td><td>

True

</td></tr><tr><td>

sn\_sec\_tisc.webhook\_max\_event\_batch\_size

</td><td>

Maximum number of events to send as part of one webhook request. The batch size will be limited to 2000 even if a higher value is set in this property.

</td><td>

Integer

</td><td>

1000

</td></tr><tr><td>

sn\_sec\_tisc.webhook\_retry\_count

</td><td>

Number of times a failed request should be retried before marking it as error and moving on to next batch of events. The retry count will be limited to 10 even if a higher number is set in this property.

</td><td>

Integer

</td><td>

5

</td></tr><tr><td>

sn\_sec\_tisc.webhook\_retry\_interval

</td><td>

Number of seconds to wait before re-attempting a failed batch.

 This will exponentially increase based on the retry count. For example, if retry\_count is 3 and retry\_interval is 30, retries are fired after 30, 60, and 120s.

 The initial retry interval will be limited to 300 seconds even if a higher value is set in this property.

</td><td>

Integer

</td><td>

30

</td></tr></tbody>
</table>**Parent Topic:**[Working with Webhooks](tisc-webhooks.md)

**Related topics**  


[Configure webhooks](setup-webhooks.md)

[Webhook Triggers](tisc-triggers.md)

