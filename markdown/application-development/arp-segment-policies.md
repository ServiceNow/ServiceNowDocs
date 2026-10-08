---
title: Segment policies
description: Segment policies enable broad access patterns across one or more Application Runtime Policy segment without requiring granular policy records for each access. If your application requires segment policies, you must create them manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/arp-segment-policies.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [segment policies, wildcard policies, ARP, Application Runtime Policy]
breadcrumb: [Explore, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Segment policies

Segment policies enable broad access patterns across one or more Application Runtime Policy segment without requiring granular policy records for each access. If your application requires segment policies, you must create them manually.

Segment policies provide a declarative way to enable broad categories of access. For example, rather than creating individual policy records for every external network call, you can create a single segment policy. This segment policy covers a certain type of access that will be allowed without a granular policy record.

When you activate a segment policy with one or more wildcard policies, ARP doesn't create individual policy records for access attempts covered by those wildcard policies. Access is granted without requiring per-resource approval.

Because they provide such broad resource access, only use segment policies when out-of-scope resources called at runtime can't be known during application development. For more information about activating segment policies, see [Create a segment policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/create-segment-policy-arp.md).

