---
title: Change the order of flow execution
description: Integration capability implementations specify the flow to be executed. In the base system, flows are executed sequentially, in the order specified in the implementation. You can change the order as needed.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Change the order of flow execution

Integration capability implementations specify the flow to be executed. In the base system, flows are executed sequentially, in the order specified in the implementation. You can change the order as needed.

## Before you begin

Role required: sn\_sec\_cmn.write

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Capabilities**.

    ![Integration Capabilities](../../security-operations-integrations/image/integration-capabilities.png)

2.  Select the integration capability for which you want to change the execution order.

    ![Integration Capability Implementations showing the execution order](../../security-operations-integrations/image/change-order.png)

3.  Select the implementation you want to modify.

    ![Integration Capability Implementation for selected implementation](../../security-operations-integrations/image/tanium.png)

4.  Change the **Order** to a higher or lower number.

    Lower numbers have a higher execution priority.

5.  Click **Submit**.


**Parent Topic:**[Integration capabilities](../concept/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability](../concept/block-request-capability.md)

[Security Operations Integration- Email Search and Delete capability](../concept/email-search-capability.md)

[Security Operations Integration- Enrich CI capability](../concept/enrich-ci-capability.md)

[Security Operations Integration- Enrich Observable capability](../concept/enrich-observable-capability.md)

[Security Operations Integration- Get Network Statistics capability](../concept/get-network-statistics-capability.md)

[Security Operations Integration- Get Running Processes capability](../concept/get-running-processes-capability.md)

[Security Operations Integration- Isolate Host capability](../concept/isolate-host-capability.md)

[Security Operations Integration- Publish to Watchlist capability](../concept/pubish-to-watchlist-capability.md)

[Security Operations Integration- Sightings Search capability](../concept/sightings-search-capability.md)

[Security Operations Integration - Threat Lookup capability](../concept/sec-ops-threat-lookups-capability.md)

