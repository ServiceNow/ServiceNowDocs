---
title: Threat Lookup - Have I been pwned? flow
description: The Threat Lookup - Have I been pwned? flow performs a lookup on selected observables. If the observables are of a type recognized by Have I been pwned?, the observables are scanned for malware, and the results are returned.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Have I been pwned? integration setup, Have I been pwned? integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Threat Lookup - Have I been pwned? flow

The Threat Lookup - Have I been pwned? flow performs a lookup on selected observables. If the observables are of a type recognized by Have I been pwned?, the observables are scanned for malware, and the results are returned.

Role required: sn\_si\_admin

This flow is triggered by the [Security Operations Integration - Threat Lookup capability](../../../security-operations-common/concept/sec-ops-threat-lookups-capability.md) when you perform a threat lookup on one or more observables, and the Have I been pwned? implementation is selected. For more information, see [Perform lookups on observables](../../../threat-intelligence/task/perform-lookups-on-observables.md).

![Security Operations - Have I been pwned flow](../image/flows-haveibeen-pwned.png "Have I been pwned flow")

For information on the activities used by this flow, see [Common Security Operations integration flows and orchestration activities](../../../security-operations-common/concept/common-wf-activities.md).

