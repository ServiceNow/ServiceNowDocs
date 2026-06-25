---
title: Change the order of flow execution
description: Integration capability implementations specify the flow to be executed. In the base system, flows are executed sequentially, in the order specified in the implementation. You can change the order as needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/change-wf-execution-order.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Change the order of flow execution

Integration capability implementations specify the flow to be executed. In the base system, flows are executed sequentially, in the order specified in the implementation. You can change the order as needed.

## Before you begin

Role required: sn\_sec\_cmn.write

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Capabilities**.

    \[Omitted image "integration-capabilities.png"\] Alt text: Integration Capabilities

2.  Select the integration capability for which you want to change the execution order.

3.  Select the implementation you want to modify.

4.  Change the **Order** to a higher or lower number.

    Lower numbers have a higher execution priority.

5.  Select **Submit**.


**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability]()

[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich CI capability]()

[Security Operations Integration- Enrich Observable capability]()

[Security Operations Integration- Get Network Statistics capability]()

[Security Operations Integration- Get Running Processes capability]()

[Security Operations Integration- Isolate Host capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Security Operations Integration - Threat Lookup capability]()

